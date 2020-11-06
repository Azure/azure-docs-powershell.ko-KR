---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: AD76C752-2070-449D-BF4F-B4260B05AB02
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoveryserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: ce38334d3ae37864d53830970d895e29755f6687
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524883"
---
# Update-AzureRmSiteRecoveryServer

## SYNOPSIS
사이트 복구 서버를 새로 고칩니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Update-AzureRmSiteRecoveryServer -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**업데이트 AzureRmSiteRecoveryServer** Cmdlet은 Azure Site Recovery 서버를 새로 고칩니다.

## 예제의

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -서버
이 cmdlet이 업데이트 하는 사이트 복구 서버를 지정 합니다.

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### ASRServer
' Server ' 매개 변수는 파이프라인에서 ' ASRServer ' 형식의 값을 허용 합니다.

## 출력

## 상속자

## 관련 링크

[Get-AzureRmSiteRecoveryServer](./Get-AzureRmSiteRecoveryServer.md)

[제거-AzureRmSiteRecoveryServer](./Remove-AzureRmSiteRecoveryServer.md)
