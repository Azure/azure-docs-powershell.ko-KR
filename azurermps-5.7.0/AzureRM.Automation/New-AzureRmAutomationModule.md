---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
ms.openlocfilehash: 91adec21cd620b0ac126a91191dba7ccdf0b3767
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702176"
---
# New-AzureRmAutomationModule

## SYNOPSIS
모듈을 자동화로 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
New-AzureRmAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**새 AzureRmAutomationModule** cmdlet은 모듈을 Azure 자동화로 가져옵니다.
이 명령은 .zip 확장명을 가진 압축 파일을 받습니다.
파일에는 다음 형식 중 하나인 파일이 포함 된 폴더가 포함 되어 있습니다. 

- 파일 이름 확장명이 psm1 또는 .dll 인 wps_2 모듈 
- psd1 파일 이름 확장명을 가진 wps_2 모듈 매니페스트

.Zip 파일의 이름과 폴더의 이름 및 폴더에 있는 파일의 이름이 동일 해야 합니다.

.Zip 파일을 자동화 서비스에서 액세스할 수 있는 URL로 지정 합니다.

이 cmdlet 또는 Set-AzureRmAutomationModule cmdlet을 사용 하 여 wps_2 모듈을 자동화로 가져오는 경우 작업이 비동기 작업입니다.
명령이 성공적으로 가져오기에 성공 또는 실패 하는지 여부를 완료 합니다.
성공 여부를 확인 하려면 다음 명령을 실행 합니다.

`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `모듈

**ProvisioningState** 속성에 성공 값이 있는지 확인 합니다.

## 예제의

### 예제 1: 모듈 가져오기
```
PS C:\>New-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

이 명령은 ContosoModule 이라는 모듈을 Contoso17 이라는 Automation 계정으로 가져옵니다.
이 모듈은 contosostorage 이라는 저장소 계정의 Azure blob에 저장 되며, 명명 된 컨테이너인 container입니다.

## 변수

### -AutomationAccountName
이 cmdlet이 모듈을 가져오는 Automation 계정의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ContentLinkUri
모듈 zip 패키지에 대 한 url입니다.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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
이 cmdlet이 가져오는 모듈의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
이 cmdlet가 모듈을 가져올 리소스 그룹의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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

### Microsoft Azure. 모듈별. 모듈

## 상속자

## 관련 링크

[Get-AzureRmAutomationModule](./Get-AzureRmAutomationModule.md)

[제거-AzureRmAutomationModule](./Remove-AzureRmAutomationModule.md)

[Set-AzureRmAutomationModule](./Set-AzureRmAutomationModule.md)


