---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
ms.openlocfilehash: 7a67d6aa0b891c78d644ec7d5f3923a354c3cef1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217727"
---
# Get-AzManagedHsm

## SYNOPSIS
관리 되는 Hsm을 받으세요.

## 구문과

```
Get-AzManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzManagedHsm** cmdlet은 구독에서 관리 되는 hsm에 대 한 정보를 가져옵니다. 구독에서 관리 되는 모든 Hsm 인스턴스를 보거나 리소스 그룹 또는 특정 관리 되는 HSM을 기준으로 결과를 필터링 할 수 있습니다.
관리 되는 단일 HSM을 가져올 때이 cmdlet에 리소스 그룹을 지정 하는 것은 선택 사항 이지만 더 나은 성능을 위해서는이 작업을 수행 해야 합니다.

## 예제의

### 예제 1: 현재 구독에서 관리 되는 모든 Hsm 가져오기
```powershell
PS C:\> Get-AzManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

이 명령은 현재 구독에서 관리 되는 모든 Hsm을 가져옵니다.

### 예제 2: 관리 되는 특정 HSM 가져오기
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

이 명령은 현재 구독에서 myhsm 이라는 관리 되는 HSM을 가져옵니다.

### 예제 3: 리소스 그룹에 관리 되는 Hsm 가져오기
```powershell
PS C:\> Get-AzManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

이 명령은 myrg1 이라는 리소스 그룹에 있는 모든 관리 되는 Hsm을 가져옵니다.

### 예제 4: 필터링을 사용 하 여 관리 되는 Hsm 가져오기
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

이 명령은 "myhsm"으로 시작 하는 구독의 관리 되는 모든 Hsm을 가져옵니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
HSM 이름. Cmdlet은 이름 및 현재 선택 된 환경에 따라 HSM의 FQDN을 생성 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
쿼리 되는 관리 되는 HSM과 연결 된 리소스 그룹의 이름을 지정 합니다.

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

### 태그
관리 되는 Hsm 목록을 필터링 하는 지정 된 태그의 키 및 선택적 값을 지정 합니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### System. 문자열

### System.webserver. 컬렉션 테이블

## 출력

### Microsoft. KeyVault. 모델. PSManagedHsm

### Microsoft. KeyVault. PSKeyVaultIdentityItem

## 상속자

## 관련 링크

[새로운 AzManagedHsm](./New-AzManagedHsm.md)

[제거-AzManagedHsm](./Remove-AzManagedHsm.md)

[업데이트-AzManagedHsm](./Update-AzManagedHsm.md)