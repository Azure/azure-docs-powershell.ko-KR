---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: baccd437f98a12376d564bee35bdb74d736ec225
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529244"
---
# New-AzureRmNotificationHubsNamespaceAuthorizationRules

## SYNOPSIS
권한 부여 규칙을 만들고 해당 규칙을 알림 허브 네임 스페이스에 할당 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### InputFileParameterSet
```
New-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SASRuleParameterSet
```
New-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureRmNotificationHubsNamespaceAuthorizationRules** CMDLET은 SAS (공유 액세스 서명) 권한 부여 규칙을 만들어 알림 허브 네임 스페이스에 할당 합니다.
권한 부여 규칙은 해당 네임 스페이스에 포함 된 알림 허브 및 네임 스페이스에 대 한 사용자 권한을 관리 합니다.

이 cmdlet은 새 권한 부여 규칙을 만들어 네임 스페이스에 할당 하는 두 가지 방법을 제공 합니다.
**Sharedaccessauthorizationruleattributes** 개체의 인스턴스를 만든 다음 새 규칙을 포함할 속성 값으로 해당 개체를 구성할 수 있습니다.
.NET Framework를 사용 하 여이 작업을 수행할 수 있습니다.
그런 다음 *SASRule* 매개 변수를 사용 하 여 해당 속성 값을 새 규칙으로 복사할 수 있습니다.

또는 관련 구성 값이 포함 된 JSON (JavaScript 개체 표시법) 파일을 만든 다음 *InputFile* 매개 변수를 사용 하 여 해당 값을 적용할 수 있습니다.
JSON 파일은 다음과 같은 구문을 사용 하는 텍스트 파일입니다.

{  
    "Name": "ContosoAuthorizationRule",  
    "PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =",  
    "권한": \[  
        "듣기",  
        보내며  
    \]  
}

앞의 JSON 샘플에서는 **AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet을 함께 사용 하는 경우 사용자가 네임 스페이스에 대 한 수신을 보내고 받을 수 있도록 하는 ContosoAuthorizationRule 라는 권한 부여 규칙을 만듭니다.
인증에 사용 되는 *PrimaryKey* 는 다음 Windows PowerShell 명령을 사용 하 여 임의로 생성할 수 있습니다.

\[Convert \] :: ToBase64String ((1.32 |% { \[ byte/] (가져오기-임의-최소 0-최대 255)))))))))

## 예제의

### 예제 1: 권한 부여 규칙을 만들어 네임 스페이스에 할당
```
PS C:\>New-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

이 명령은 권한 부여 규칙을 만들고이 규칙을 네임 스페이스 ContosoNamespace에 할당 합니다.
이 규칙을 만들 때 네임 스페이스에 할당 되는 적절 한 네임 스페이스와 리소스 그룹을 지정 해야 합니다.
그러나 규칙 자체에 대 한 정보를 지정할 필요는 없습니다. C:\Configuration\NamespaceAuthorizationRules.js입력 파일에서 규칙 정보를 가져옵니다.

## 변수

### -InputFile
새 권한 부여 규칙에 대 한 구성 정보를 포함 하는 JSON 파일의 경로를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
권한 부여 규칙이 할당 되는 네임 스페이스를 지정 합니다.

네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.
새 규칙을 기존 네임 스페이스에 할당 해야 합니다.
**AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet이 새 네임 스페이스를 만들 수 없습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
네임 스페이스를 할당할 리소스 그룹을 지정 합니다.

리소스 그룹은 관리 및 Azure 관리를 쉽게 할 수 있는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.

기존 리소스 그룹을 사용 해야 합니다.
이 cmdlet은 새 리소스 그룹을 만들 수 없습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SASRule
새 규칙에 대 한 구성 정보를 포함 하는 **Sharedaccessauthorizationruleattributes** 개체를 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### Microsoft. Azure. 명령. SharedAccessAuthorizationRuleAttributes

## 상속자

## 관련 링크

[Get-AzureRmNotificationHubAuthorizationRules](./Get-AzureRmNotificationHubAuthorizationRules.md)

[제거-AzureRmNotificationHubAuthorizationRules](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[Set-AzureRmNotificationHubAuthorizationRules](./Set-AzureRmNotificationHubAuthorizationRules.md)


