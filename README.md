# Spam-report-facebook
Spam report someone
                    print(f"[ {magenta}{time_rn}{reset} ] | ( {red}-{reset} ) {yellow}Cannot report to ", end='')
                    sys.stdout.flush()
                    Write.Print(f"{username} ~ {iduser}\n", Colors.purple_to_red, interval=0.000)
                    failed += 1
                    total += 1
                    update_console_title()
                    mass_report()
        else:
            mass_report()  
    except Exception as e:
        failed += 1
        total += 1
        update_console_title()
        mass_report()

def mass_report_thread():
    mass_report()

def check_ui_thread():
    check_ui()

num_threads = data['threads']
threads = []

with threading.Lock():
    for _ in range(num_threads - 1):
        thread = threading.Thread(target=mass_report_thread)
        thread.start()
        threads.append(thread)

    check_ui_thread = threading.Thread(target=check_ui_thread)
    check_ui_thread.start()
    threads.append(check_ui_thread)

    for thread in threads:
        thread.join()                    print(f"[ {magenta}{time_rn}{reset} ] | ( {red}-{reset} ) {yellow}Cannot report to ", end='')
                    sys.stdout.flush()
                    Write.Print(f"{username} ~ {iduser}\n", Colors.purple_to_red, interval=0.000)
                    failed += 1
                    total += 1
                    update_console_title()
                    mass_report()
        else:
            mass_report()  
    except Exception as e:
        failed += 1
        total += 1
        update_console_title()
        mass_report()

def mass_report_thread():
    mass_report()

def check_ui_thread():
    check_ui()

num_threads = data['threads']
threads = []

with threading.Lock():
    for _ in range(num_threads - 1):
        thread = threading.Thread(target=mass_report_thread)
        thread.start()
        threads.append(thread)

    check_ui_thread = threading.Thread(target=check_ui_thread)
    check_ui_thread.start()
    threads.append(check_ui_thread)

    for thread in threads:
        thread.join()
