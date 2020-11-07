---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: d57f672ef440515e69535503f006e08b4c924646
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875813"
---
# <span data-ttu-id="8faf2-101">Remove-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8faf2-101">Remove-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="8faf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8faf2-102">SYNOPSIS</span></span>
<span data-ttu-id="8faf2-103">키 보관소 관리 Azure 저장소 계정 및 모든 관련 SAS 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8faf2-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

## <span data-ttu-id="8faf2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8faf2-104">SYNTAX</span></span>

```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8faf2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8faf2-105">DESCRIPTION</span></span>
<span data-ttu-id="8faf2-106">키 자격 증명 모음에서 Azure Storage 계정의 분리를 끊습니다.</span><span class="sxs-lookup"><span data-stu-id="8faf2-106">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="8faf2-107">Azure 저장소 계정이 제거 되는 것이 아니라 Azure 키 자격 증명 모음에서 관리 되는 계정 키가 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8faf2-107">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="8faf2-108">연결 된 모든 키 보관소 관리 저장소 SAS 정의도 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8faf2-108">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="8faf2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8faf2-109">EXAMPLES</span></span>

### <span data-ttu-id="8faf2-110">예제 1: 키 보관소를 관리 하는 Azure Storage 계정 및 모든 관련 SAS 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8faf2-110">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
```
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="8faf2-111">' Mystorageaccount '의 Azure 저장소 계정 및 키 보관소에서 키를 관리 하는 것을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="8faf2-111">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="8faf2-112">계정 ' mystorageaccount '는 제거 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8faf2-112">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="8faf2-113">이 계정에 연결 된 모든 키 자격 증명 모음 관리 저장소 SAS 정의가 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8faf2-113">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="8faf2-114">예제 2: 키 자격 증명 모음 관리 Azure 저장소 계정 및 모든 관련 SAS 정의를 사용자 확인 없이 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8faf2-114">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
```
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Force -Confirm:$False
```

<span data-ttu-id="8faf2-115">' Mystorageaccount '의 Azure 저장소 계정 및 키 보관소에서 키를 관리 하는 것을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="8faf2-115">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="8faf2-116">계정 ' mystorageaccount '는 제거 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8faf2-116">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="8faf2-117">이 계정에 연결 된 모든 키 자격 증명 모음 관리 저장소 SAS 정의가 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8faf2-117">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

## <span data-ttu-id="8faf2-118">변수</span><span class="sxs-lookup"><span data-stu-id="8faf2-118">PARAMETERS</span></span>

### <span data-ttu-id="8faf2-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8faf2-119">-AccountName</span></span>
<span data-ttu-id="8faf2-120">키 자격 증명 모음 관리 저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8faf2-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="8faf2-121">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 manged 저장소 계정 이름에서 관리 되는 저장소 계정 이름의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8faf2-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8faf2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8faf2-122">-DefaultProfile</span></span>
<span data-ttu-id="8faf2-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8faf2-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8faf2-124">-Force</span><span class="sxs-lookup"><span data-stu-id="8faf2-124">-Force</span></span>
<span data-ttu-id="8faf2-125">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8faf2-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8faf2-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8faf2-126">-PassThru</span></span>
<span data-ttu-id="8faf2-127">Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8faf2-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="8faf2-128">이 스위치가 지정 된 경우 cmdlet은 삭제 된 관리 저장소 계정을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8faf2-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="8faf2-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8faf2-129">-VaultName</span></span>
<span data-ttu-id="8faf2-130">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="8faf2-130">Vault name.</span></span>
<span data-ttu-id="8faf2-131">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8faf2-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="8faf2-132">-확인</span><span class="sxs-lookup"><span data-stu-id="8faf2-132">-Confirm</span></span>
<span data-ttu-id="8faf2-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8faf2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8faf2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8faf2-134">-WhatIf</span></span>
<span data-ttu-id="8faf2-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8faf2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8faf2-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8faf2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8faf2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8faf2-137">CommonParameters</span></span>
<span data-ttu-id="8faf2-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8faf2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8faf2-139">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8faf2-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8faf2-140">입력</span><span class="sxs-lookup"><span data-stu-id="8faf2-140">INPUTS</span></span>

### <span data-ttu-id="8faf2-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8faf2-141">System.String</span></span>

## <span data-ttu-id="8faf2-142">출력</span><span class="sxs-lookup"><span data-stu-id="8faf2-142">OUTPUTS</span></span>

### <span data-ttu-id="8faf2-143">Microsoft. KeyVault. \* ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8faf2-143">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="8faf2-144">상속자</span><span class="sxs-lookup"><span data-stu-id="8faf2-144">NOTES</span></span>

## <span data-ttu-id="8faf2-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8faf2-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

