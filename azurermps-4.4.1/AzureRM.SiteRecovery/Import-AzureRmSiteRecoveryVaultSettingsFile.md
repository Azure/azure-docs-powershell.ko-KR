---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 070DA86E-9EA4-4777-9D53-64B58B4401B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 42863e0dbf6982ced1f77f916c97ed4fc19d6979
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536168"
---
# Import-AzureRmSiteRecoveryVaultSettingsFile

## SYNOPSIS
사이트 복구 자격 증명 모음 설정 파일을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Import-AzureRmSiteRecoveryVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzureRmSiteRecoveryVaultSettingsFile** Cmdlet은 Azure Site recovery 자격 증명 모음 설정 파일을 가져와 현재 세션의 후속 사이트 복구 작업에 대 한 자격 증명 모음 컨텍스트를 설정 합니다.

## 예제의

## 변수

### -Path
사이트 복구 자격 증명 모음 설정 파일의 경로를 지정 합니다.
이 파일은 사이트 복구 자격 증명 모음 포털에서 다운로드 하 여 로컬에 저장할 수 있습니다.

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

### SiteRecovery. ASRVaultSettings

## 상속자

## 관련 링크

[Get-AzureRmSiteRecoveryVaultSettingsFile](./Get-AzureRmSiteRecoveryVaultSettingsFile.md)
