---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetablesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
ms.openlocfilehash: bf17a44b4f67d545ed464670776a5fc4c81b315a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190833"
---
# New-AzStorageTableSASToken

## SYNOPSIS
Azure Storage 테이블에 대한 SAS 토큰을 생성합니다.

## 구문

### SasPolicy
```
New-AzStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SasPermission
```
New-AzStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**New-AzStorageTableSASToken** cmdlet은 Azure Storage 테이블에 대한 SAS(공유 액세스 서명) 토큰을 생성합니다.

## 예제

### 예제 1: 테이블에 대한 모든 권한이 있는 SAS 토큰 생성
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

이 명령은 ContosoResources라는 테이블에 대한 모든 권한이 있는 SAS 토큰을 생성합니다.
해당 토큰은 읽기, 추가, 업데이트 및 삭제 권한을 위한 것입니다.

### 예제 2: 파티션 범위에 대한 SAS 토큰 생성
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

이 명령은 ContosoResources라는 테이블에 대한 모든 권한을 사용하여 SAS 토큰을 생성합니다.
이 명령은 *StartPartitionKey 및 EndPartitionKey* 매개 변수가 지정하는 범위로 토큰을 제한합니다. 

### 예제 3: 테이블에 대해 저장된 액세스 정책이 있는 SAS 토큰 생성
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

이 명령은 ContosoResources라는 테이블에 대한 SAS 토큰을 생성합니다.
이 명령은 ClientPolicy01이라는 저장된 액세스 정책을 지정합니다.

## PARAMETERS

### -Context
Azure 저장소 컨텍스트를 지정합니다.
저장소 컨텍스트를 얻습니다. New-AzStorageContext cmdlet을 사용 합니다.

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

### -EndPartitionKey
이 cmdlet에서 만드는 토큰에 대한 범위 끝의 파티션 키를 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndRowKey
이 cmdlet에서 만드는 토큰의 범위 끝에 대한 행 키를 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpiryTime
SAS 토큰이 만료되는 경우를 지정합니다.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FullUri
이 cmdlet이 SAS 토큰을 사용하여 전체 큐 URI를 반환하는지 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPAddressOrRange
요청을 수락할 IP 주소 또는 IP 주소 범위를 지정합니다(예: 168.1.5.65 또는 168.1.5.60-168.1.5.70).
범위는 포괄적입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Azure Storage 테이블의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 테이블에 대한 SAS 토큰을 만듭니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Permission
Azure Storage 테이블에 대한 권한을 지정합니다.
이 문자열은 읽기, 쓰기 및 삭제와 같은 `rwd` 문자열입니다.

```yaml
Type: System.String
Parameter Sets: SasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Policy
이 SAS 토큰에 대한 사용 권한을 포함하는 저장된 액세스 정책을 지정합니다.

```yaml
Type: System.String
Parameter Sets: SasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol
요청에 허용되는 프로토콜을 지정합니다.
이 매개 변수에 허용되는 값은
* HttpsOnly
* HttpsOrHttp 기본값은 HttpsOrHttp입니다.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Cosmos.Table.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartPartitionKey
이 cmdlet에서 만드는 토큰에 대한 범위의 시작 부분의 파티션 키를 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartRowKey
이 cmdlet에서 만드는 토큰의 범위 시작에 대한 행 키를 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
SAS 토큰이 유효한 경우를 지정합니다.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## 출력

### System.String

## 참고 사항

## 관련 링크

[New-AzStorageContext](./New-AzStorageContext.md)
