---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunHistory.md
ms.openlocfilehash: 60c58d6e5cd395d60818c7d7777fe561259feb15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525079"
---
# Get-AzureRmLogicAppRunHistory

## SYNOPSIS
논리 앱의 실행 기록을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmLogicAppRunHistory** cmdlet은 로직 앱의 실행 기록을 가져옵니다.
이 cmdlet은 **Workflowrun** 개체의 컬렉션을 반환 합니다.
논리 앱 및 리소스 그룹을 지정 합니다.

이 모듈은 동적 매개 변수를 지원 합니다.
동적 매개 변수를 사용 하려면 명령에 입력 합니다.
동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.
필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.

## 예제의

### 예제 1: 논리 앱의 실행 기록 가져오기
```
PS C:\>Get-AzureRmLogicAppActionRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952540

CorrelationId    : d3ddc917-9aaa-47b3-8814-c621c2ae530b
EndTime          : 1/13/2016 2:42:56 PM
Error            : {code, message}
Name             : 08587489107100664541
Outputs          : {}
StartTime        : 1/13/2016 2:42:55 PM
Status           : Failed
TriggerName      : httpTrigger
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

이 명령은 LogicApp03 이라는 논리 앱의 실행 기록을 가져옵니다.

### 예제 2: 논리 앱 실행 가져오기
```
PS C:\>Get-AzureRmLogicAppActionRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -RunName "08587489104702792076"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

이 명령은 LogicApp03 이라는 논리 앱에 대해 실행 되는 특정 논리 앱을 가져옵니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
이 cmdlet이 실행 기록을 가져오는 논리 앱의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
논리 앱을 포함 하는 리소스 그룹의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RunName
논리 앱의 실행 이름을 지정 합니다.
이 cmdlet은이 cmdlet에서 지정 하는 워크플로 실행을 가져옵니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

### Microsoft. Azure. i a m. 모델. WorkflowRun

## 상속자

## 관련 링크

[Get-AzureRmLogicAppRunAction](./Get-AzureRmLogicAppRunAction.md)

[시작-AzureRmLogicApp](./Start-AzureRmLogicApp.md)

[중지-AzureRmLogicAppRun](./Stop-AzureRmLogicAppRun.md)


