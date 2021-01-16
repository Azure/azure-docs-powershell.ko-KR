---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 2e444fba12f0ffebfd3d6679293cac31fc574e93
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324925"
---
# Get-AzStorageShareStoredAccessPolicy

## SYNOPSIS
저장소 공유에 대한 저장된 액세스 정책을 얻습니다.

## 구문

```
Get-AzStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## 설명
**Get-AzStorageShareStoredAccessPolicy** cmdlet은 Azure Storage 공유에 대한 저장된 액세스 정책을 얻습니다.
특정 정책을 얻습니다. 이름을 사용하여 지정합니다.

## 예제

### 예제 1: 공유에 저장된 액세스 정책 얻기
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

이 명령은 ContosoShare에서 GeneralPolicy라는 저장된 액세스 정책을 얻습니다.

### 예제 2: 공유에 저장된 모든 액세스 정책 얻기
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

이 명령은 ContosoShare에 저장된 모든 액세스 정책을 얻습니다.

## PARAMETERS

### -ClientTimeoutPerRequest
하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.
이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.
이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
최대 동시 네트워크 호출을 지정합니다.
이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다.
지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다.
이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.
기본값은 10입니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Context
Azure Storage 컨텍스트를 지정합니다.
컨텍스트를 얻습니다. [New-AzStorageContext](./New-AzStorageContext.md) cmdlet을 사용 합니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Policy
이 cmdlet에서 얻을 저장된 액세스 정책의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
요청의 서버 부분에 대한 시간 제한 기간의 길이를 지정합니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShareName
이 cmdlet에서 정책을 받을 저장소 공유 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## 출력

### Microsoft.Azure.Storage.File.SharedAccessFilePolicy

## 참고 사항

## 관련 링크

[New-AzStorageContext](./New-AzStorageContext.md)

[New-AzStorageShareStoredAccessPolicy](./New-AzStorageShareStoredAccessPolicy.md)

[Remove-AzStorageShareStoredAccessPolicy](./Remove-AzStorageShareStoredAccessPolicy.md)

[Set-AzStorageShareStoredAccessPolicy](./Set-AzStorageShareStoredAccessPolicy.md)
