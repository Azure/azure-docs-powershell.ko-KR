---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
ms.openlocfilehash: 61c58d4dae5d990a72ca81e7016a3e312e82229a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880445"
---
# <span data-ttu-id="9d753-101">Remove-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="9d753-101">Remove-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="9d753-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d753-102">SYNOPSIS</span></span>
<span data-ttu-id="9d753-103">키 보관소 관리 Azure 저장소 SAS 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d753-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d753-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9d753-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d753-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9d753-105">DESCRIPTION</span></span>
<span data-ttu-id="9d753-106">키 보관소 관리 Azure 저장소 SAS 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d753-106">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="9d753-107">이는이 SAS 정의에 따라 SAS 토큰을 가져오는 데 사용 되는 비밀도 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d753-107">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="9d753-108">예제의</span><span class="sxs-lookup"><span data-stu-id="9d753-108">EXAMPLES</span></span>

### <span data-ttu-id="9d753-109">예제 1: 키 보관소 관리 Azure 저장소 SAS 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d753-109">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef'
```

<span data-ttu-id="9d753-110">자격 증명 모음 ' mystorageaccount '와 연결 된 키 보관소 관리 저장소 SAS 정의 ' mysasdef '를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d753-110">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="9d753-111">예제 2: 사용자 확인 없이 키 자격 증명 관리 Azure 저장소 SAS 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d753-111">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -Force -Confirm:$False
```

<span data-ttu-id="9d753-112">자격 증명 모음 ' mystorageaccount '와 연결 된 키 보관소 관리 저장소 SAS 정의 ' mysasdef '를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d753-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="9d753-113">변수</span><span class="sxs-lookup"><span data-stu-id="9d753-113">PARAMETERS</span></span>

### <span data-ttu-id="9d753-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9d753-114">-AccountName</span></span>
<span data-ttu-id="9d753-115">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9d753-115">Storage account name.</span></span>
<span data-ttu-id="9d753-116">Cmdlet은 관리 되는 저장소 계정 이름의 FQDN을 자격 증명 모음 이름, 현재 선택한 환경 및 저장소 계정 이름과 동일 하 게 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9d753-116">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d753-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d753-117">-DefaultProfile</span></span>
<span data-ttu-id="9d753-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9d753-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d753-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9d753-119">-Force</span></span>
<span data-ttu-id="9d753-120">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9d753-120">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d753-121">-이름</span><span class="sxs-lookup"><span data-stu-id="9d753-121">-Name</span></span>
<span data-ttu-id="9d753-122">저장소 sas 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9d753-122">Storage sas definition name.</span></span>
<span data-ttu-id="9d753-123">Cmdlet은 자격 증명 모음 이름, 현재 선택 된 환경, 저장소 계정 이름 및 sas 정의 이름에서 저장소 sas 정의의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d753-123">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d753-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d753-124">-PassThru</span></span>
<span data-ttu-id="9d753-125">Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9d753-125">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="9d753-126">이 스위치가 지정 된 경우 cmdlet은 삭제 된 관리 저장소 계정을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d753-126">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d753-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9d753-127">-VaultName</span></span>
<span data-ttu-id="9d753-128">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="9d753-128">Vault name.</span></span>
<span data-ttu-id="9d753-129">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d753-129">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="9d753-130">-확인</span><span class="sxs-lookup"><span data-stu-id="9d753-130">-Confirm</span></span>
<span data-ttu-id="9d753-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d753-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d753-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d753-132">-WhatIf</span></span>
<span data-ttu-id="9d753-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9d753-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d753-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9d753-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d753-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d753-135">CommonParameters</span></span>
<span data-ttu-id="9d753-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d753-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d753-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d753-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d753-138">입력</span><span class="sxs-lookup"><span data-stu-id="9d753-138">INPUTS</span></span>

### <span data-ttu-id="9d753-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9d753-139">System.String</span></span>

## <span data-ttu-id="9d753-140">출력</span><span class="sxs-lookup"><span data-stu-id="9d753-140">OUTPUTS</span></span>

### <span data-ttu-id="9d753-141">Microsoft. KeyVault. ' Managed' 모델. i 볼트로 Esasdefinition</span><span class="sxs-lookup"><span data-stu-id="9d753-141">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="9d753-142">상속자</span><span class="sxs-lookup"><span data-stu-id="9d753-142">NOTES</span></span>

## <span data-ttu-id="9d753-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9d753-143">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

