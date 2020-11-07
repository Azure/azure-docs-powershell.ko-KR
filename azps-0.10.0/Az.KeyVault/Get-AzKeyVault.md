---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-Azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
ms.openlocfilehash: aaace602cd50f9464021b1dcbefe39272e1621bb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875844"
---
# Get-AzKeyVault

## SYNOPSIS
키 볼트를 가져옵니다.

## 구문과

### GetVaultByName
```
Get-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByDeletedVault
```
Get-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListVaultsByResourceGroup
```
Get-AzKeyVault [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ListAllDeletedVaultsInSubscription
```
Get-AzKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListAllVaultsInSubscription
```
Get-AzKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzKeyVault** cmdlet은 구독의 키 자격 증명 모음에 대 한 정보를 가져옵니다. 구독에서 모든 키 보관소 인스턴스를 보거나 리소스 그룹 또는 특정 키 보관소를 기준으로 결과를 필터링 할 수 있습니다.

단일 키 자격 증명 모음을 가져올 때이 cmdlet에 리소스 그룹을 지정 하는 것은 선택 사항 이지만 성능이 더 나은 지 확인 해야 합니다.

## 예제의

### 예제 1: 현재 구독의 모든 키 보관소 가져오기
```
PS C:\>Get-AzKeyVault
```

이 명령은 현재 구독의 모든 키 보관소를 가져옵니다.

### 예제 2: 특정 키 보관소 가져오기
```
PS C:\>$MyVault = Get-AzKeyVault -VaultName 'Contoso03Vault'
```

이 명령은 현재 구독에서 Contoso03Vault 이라는 키 보관소를 가져온 다음이를 $MyVault 변수에 저장 합니다. $MyVault의 속성을 검사 하 여 키 자격 증명 모음에 대 한 세부 정보를 얻을 수 있습니다.

### 예제 3: 리소스 그룹의 키 보관소 가져오기
```
PS C:\>Get-AzKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

이 명령은 ContosoPayRollResourceGroup 이라는 리소스 그룹의 모든 키 보관소를 가져옵니다.

### 예제 4: 현재 구독에서 삭제 된 모든 키 보관소 가져오기
```
PS C:\>Get-AzKeyVault -InRemovedState
```

이 명령은 현재 구독에서 삭제 된 모든 키 보관소를 가져옵니다.

### 예제 5: 삭제 된 키 보관소 가져오기
```
PS C:\>Get-AzKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

이 명령은 현재 구독과 eastus2 지역에서 Contoso03Vault 이라는 삭제 된 키 보관소 정보를 가져옵니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InRemovedState
이전에 삭제 된 자격 증명을 출력에 표시할지 여부를 지정 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -위치
삭제 된 자격 증명 모음의 위치입니다.

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
쿼리할 키 자격 증명 또는 키 보관소와 연결 된 리소스 그룹의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: GetVaultByName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListVaultsByResourceGroup
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### 태그
해시 테이블 형태의 키-값 쌍입니다. 예를 들어:

@ {key0 = "value0", key1 = $null, key2 = "value2"}

```yaml
Type: Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
키 보관소의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: GetVaultByName, ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

### Microsoft. KeyVault. PSVault

### PSVaultIdentityItem의 ' 1 [Microsoft Azure.] 목록. List.

### Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault

### EletedVault의 List ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSD]

## 상속자

## 관련 링크

[새로운 AzKeyVault](./New-AzKeyVault.md)

[제거-AzKeyVault](./Remove-AzKeyVault.md)
