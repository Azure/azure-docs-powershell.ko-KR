---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragecontaineracl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
ms.openlocfilehash: 23aa7e6df5aae820980551db445339ade34ac779
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002267"
---
# Set-AzStorageContainerAcl

## SYNOPSIS
저장소 컨테이너에 대한 공용 액세스 권한을 설정합니다.

## 구문

```
Set-AzStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## 설명
**Set-AzStorageContainerAcl** cmdlet은 Azure에서 지정된 저장소 컨테이너에 대한 공용 액세스 권한을 설정합니다.

## 예제

### 예제 1: 이름에 따라 Azure Storage 컨테이너 ACL 설정
```
PS C:\>Set-AzStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

이 명령은 공용 액세스 권한이 없는 컨테이너를 만듭니다.

### 예제 2: 파이프라인을 사용하여 Azure Storage 컨테이너 ACL 설정
```
PS C:\>Get-AzStorageContainer container* | Set-AzStorageContainerAcl -Permission Blob -PassThru
```

이 명령은 이름이 컨테이너로 시작한 다음 파이프라인에서 결과를 전달하여 모든 저장소 컨테이너에 대한 권한을 Blob 액세스로 설정합니다.

## 매개 변수

### -ClientTimeoutPerRequest
하나의 서비스 요청에 대해 클라이언트 쪽 시간 간격(초)을 지정합니다.
지정된 간격에서 이전 호출이 실패하면 이 cmdlet에서 요청을 다시 검색합니다.
간격이 경과하기 전에 이 cmdlet에서 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.

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
이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 로컬 CPU 및 대역폭 사용량을 제한하는 동시성 제한할 수 있습니다.
지정된 값은 절대 개수로 코어 수에 곱하지 않습니다.
이 매개 변수는 초당 100킬로비트와 같은 대역폭이 낮은 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.
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
New-AzStorageContext cmdlet을 사용하여 만들 수 있습니다.

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
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -Name
컨테이너 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -PassThru
작업하는 항목을 나타내는 개체를 반환합니다.
기본적으로 이 cmdlet은 출력을 생성하지 않습니다.

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

### -권한
이 컨테이너에 대한 공용 액세스 수준을 지정합니다.
기본적으로 컨테이너 및 해당 컨테이너의 모든 Blob은 저장소 계정 소유자만 액세스할 수 있습니다.
익명 사용자에게 컨테이너 및 해당 Blob에 대한 읽기 권한을 부여하려면 공용 액세스를 사용하도록 컨테이너 권한을 설정할 수 있습니다.
익명 사용자는 요청을 인증하지 않고 공개적으로 사용 가능한 컨테이너에서 Blob을 읽을 수 있습니다.
이 매개 변수에 대해 허용되는 값은 --Container입니다.
컨테이너 및 해당 Blob에 대한 전체 읽기 액세스를 제공합니다.
클라이언트는 익명 요청을 통해 컨테이너에 Blob을 열소할 수 있지만 저장소 계정에서 컨테이너를 열 수 없습니다. --Blob.
익명 요청을 통해 컨테이너의 Blob 데이터에 대한 읽기 액세스를 제공하지만 컨테이너 데이터에 대한 액세스는 제공하지 않습니다.
클라이언트는 익명 요청을 사용하여 컨테이너에 Blob을 열소할 수 없습니다. --Off.
저장소 계정 소유자만 액세스를 제한합니다.

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
요청에 대해 서비스 쪽 시간 시간 간격(초)을 지정합니다.
서비스가 요청을 처리하기 전에 지정된 간격이 경과하면 저장소 서비스가 오류를 반환합니다.
각 요청에 대한 서버 쪽 시간 시간입니다.

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## 출력

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer

## 참고 사항

## 관련 링크

[Get-AzStorageContainer](./Get-AzStorageContainer.md)

[New-AzStorageContainer](./New-AzStorageContainer.md)

[Remove-AzStorageContainer](./Remove-AzStorageContainer.md)


