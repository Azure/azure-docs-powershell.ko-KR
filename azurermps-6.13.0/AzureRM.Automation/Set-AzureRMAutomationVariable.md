---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationVariable.md
ms.openlocfilehash: 462566749ce0c55d4f892cc19e362f62b6fd0fa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524616"
---
# Set-AzureRmAutomationVariable

## SYNOPSIS
자동화 변수를 수정 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### UpdateVariableValue
```
Set-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### UpdateVariableDescription
```
Set-AzureRmAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmAutomationVariable** Cmdlet은 Azure Automation에서 변수의 값 또는 설명을 수정 합니다.
변수를 암호화 하려면 *암호화* 된 매개 변수를 지정 합니다.
생성 후 변수의 암호화 된 상태를 수정할 수 없습니다.
암호화 되지 않은 기존 변수에 대해 *암호화* 를 지정 하면 실패 합니다.

## 예제의

### 예제 1: 변수 값 설정
```
PS C:\>Set-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

이 명령은 Contoso17 이라는 Azure Automation 계정의 StringVariable22 라는 변수에 대해 새 값을 설정 합니다.

## 변수

### -AutomationAccountName
변수가 저장 된 Automation 계정의 이름을 지정 합니다.

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

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

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

### -설명
변수에 대 한 설명을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: UpdateVariableDescription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### 암호화 된
Cmdlet이 저장소의 변수 값을 암호화할지 여부를 지정 합니다.

```yaml
Type: System.Boolean
Parameter Sets: UpdateVariableValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
이 cmdlet이 수정 하는 변수의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
이 cmdlet이 변수를 수정할 리소스 그룹을 지정 합니다.

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

### -값
변수의 값을 지정 합니다.

```yaml
Type: System.Object
Parameter Sets: UpdateVariableValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### 시스템 부울

### System. 개체

## 출력

### Microsoft. Azure. m a. 모델 변수

## 상속자

## 관련 링크

[Get-AzureRmAutomationVariable](./Get-AzureRMAutomationVariable.md)

[새로운 AzureRmAutomationVariable](./New-AzureRMAutomationVariable.md)

[제거-AzureRmAutomationVariable](./Remove-AzureRMAutomationVariable.md)


