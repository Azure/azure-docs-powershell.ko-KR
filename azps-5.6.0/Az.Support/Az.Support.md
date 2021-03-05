---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: b02401044f3b01a73954ac199cc15457cddb795a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979115"
---
# Az.Support 모듈
## 설명
이 섹션의 항목에서는 Azure Resource Manager(azure Resource Manager) 프레임워크에서 Azure 지원 티켓을 만들고 관리하기 위한 Azure PowerShell cmdlet을 ARM 설명합니다. cmdlet은 Microsoft.Azure.Commands.Support 네임스페이스에 있습니다.

## Az.Support Cmdlet
### [Get-AzSupportService](Get-AzSupportService.md)
지원이 가능한 Azure 서비스의 현재 목록을 받습니다. 각 Azure 서비스에는 문제 분류라는 자체 범주 집합이 있습니다. Get-AzSupportProblemClassification을 사용하여 서비스에 대한 현재 문제 분류 목록을 얻습니다. 서비스 및 문제 분류 GUID를 사용하여 New-AzSupportTicket을 사용하여 새 지원 티켓을 만들 수 있습니다.

### [Get-AzSupportProblemClassification](Get-AzSupportProblemClassification.md)
Azure 서비스에 대한 현재 문제 분류 목록을 얻습니다. 서비스 및 문제 분류 GUID를 사용하여 New-AzSupportTicket을 사용하여 새 지원 티켓을 만들 수 있습니다. 

### [New-AzSupportContactProfileObject](New-AzSupportContactProfileObject.md)
도우미 cmdlet을 사용하여 지원 연락처 프로필 개체를 만듭니다. 이 개체를 cmdlet에 New-AzSupportTicket 수 있습니다.

### [New-AzSupportTicket](New-AzSupportTicket.md)
새 Azure 지원 티켓을 만듭니다. 이 작업은 Azure New 지원 요청 페이지의 동작을 [모델링합니다.](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)

### [Get-AzSupportTicket](Get-AzSupportTicket.md)
지원 티켓 목록을 받습니다. 티켓 이름으로 전체 지원 티켓 세부 정보를 얻거나  상태 또는 *CreatedDate로* 지원 티켓을 필터링할 수 있습니다.

### [Update-AzSupportTicket](Update-AzSupportTicket.md)
지원 티켓의 심각도, 상태 또는 고객 연락처 세부 정보를 업데이트합니다.

### [Get-AzSupportTicketCommunication](Get-AzSupportTicketCommunication.md)
지원 티켓에 대한 통신을 받습니다. *CreatedDate* 또는 CommunicationType 을 사용하여 지원 티켓 통신을 *필터링할 수도 있습니다.* 

### [New-AzSupportTicketCommunication](New-AzSupportTicketCommunication.md)
Azure 지원 티켓에 새 고객 통신을 추가합니다. 



