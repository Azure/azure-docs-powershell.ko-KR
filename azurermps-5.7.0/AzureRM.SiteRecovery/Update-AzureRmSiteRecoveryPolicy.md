---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 313E7444-2EB4-4B91-9E56-5730CB006046
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: b4e6cff174f0bb623145a4b364b2c22297530c51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524888"
---
# Update-AzureRmSiteRecoveryPolicy

## SYNOPSIS

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Update-AzureRmSiteRecoveryPolicy -Policy <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은

## 예제의

## 변수

### -ApplicationConsistentSnapshotFrequencyInHours
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -인증
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -압축
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -암호화
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -정책
```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecoveryAzureStorageAccountId
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPoints
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicaDeletion
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationFrequencyInSeconds
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationMethod
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationPort
```yaml
Type: UInt16
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationStartTime
```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### ASRPolicy
' Policy ' 매개 변수는 파이프라인에서 ' ASRPolicy ' 형식의 값을 허용 합니다.

## 출력

## 상속자

## 관련 링크

