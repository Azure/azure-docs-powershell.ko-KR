---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/update-AzKeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: d73e9b02940f98db6734f851219399a2ba6c74a2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876675"
---
# <span data-ttu-id="c34ce-101">Update-AzKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c34ce-101">Update-AzKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="c34ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c34ce-102">SYNOPSIS</span></span>
<span data-ttu-id="c34ce-103">키 자격 증명 모음 관리 Azure 저장소 계정의 지정 된 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c34ce-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="c34ce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c34ce-104">SYNTAX</span></span>

```
Update-AzKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c34ce-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c34ce-105">DESCRIPTION</span></span>
<span data-ttu-id="c34ce-106">키 보관소의 지정 된 키를 관리 하는 Azure Storage 계정을 다시 생성 하 고 키를 활성 키로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c34ce-106">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="c34ce-107">키 보관소는 키를 다시 생성 하기 위해 Azure Resource Manager에 대 한 통화를 프록시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c34ce-107">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="c34ce-108">호출자는 지정 된 Azure Storage 계정에서 키를 다시 생성 하는 권한을 플랫폼이 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c34ce-108">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="c34ce-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c34ce-109">EXAMPLES</span></span>

### <span data-ttu-id="c34ce-110">예제 1: 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="c34ce-110">Example 1: Regenerate a key</span></span>
```
PS C:\> Update-AzKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'
```

<span data-ttu-id="c34ce-111">계정 ' mystorageaccount '의 ' key1 '을 다시 생성 하 고 ' key1 '을 키 보관소 관리 Azure 저장소 계정의 활성으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c34ce-111">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="c34ce-112">변수</span><span class="sxs-lookup"><span data-stu-id="c34ce-112">PARAMETERS</span></span>

### <span data-ttu-id="c34ce-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c34ce-113">-AccountName</span></span>
<span data-ttu-id="c34ce-114">키 자격 증명 모음 관리 저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c34ce-114">Key Vault managed storage account name.</span></span> <span data-ttu-id="c34ce-115">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 manged 저장소 계정 이름에서 관리 되는 저장소 계정 이름의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c34ce-115">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="c34ce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c34ce-116">-DefaultProfile</span></span>
<span data-ttu-id="c34ce-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c34ce-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c34ce-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c34ce-118">-Force</span></span>
<span data-ttu-id="c34ce-119">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c34ce-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c34ce-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="c34ce-120">-KeyName</span></span>
<span data-ttu-id="c34ce-121">다시 생성 하 고 활성 상태로 만들 저장소 계정 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c34ce-121">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c34ce-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c34ce-122">-PassThru</span></span>
<span data-ttu-id="c34ce-123">Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c34ce-123">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="c34ce-124">이 스위치가 지정 된 경우 cmdlet은 삭제 된 관리 저장소 계정을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c34ce-124">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="c34ce-125">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c34ce-125">-VaultName</span></span>
<span data-ttu-id="c34ce-126">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="c34ce-126">Vault name.</span></span>
<span data-ttu-id="c34ce-127">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c34ce-127">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="c34ce-128">-확인</span><span class="sxs-lookup"><span data-stu-id="c34ce-128">-Confirm</span></span>
<span data-ttu-id="c34ce-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c34ce-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c34ce-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c34ce-130">-WhatIf</span></span>
<span data-ttu-id="c34ce-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c34ce-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c34ce-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c34ce-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c34ce-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c34ce-133">CommonParameters</span></span>
<span data-ttu-id="c34ce-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c34ce-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c34ce-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c34ce-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c34ce-136">입력</span><span class="sxs-lookup"><span data-stu-id="c34ce-136">INPUTS</span></span>

### <span data-ttu-id="c34ce-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c34ce-137">System.String</span></span>

## <span data-ttu-id="c34ce-138">출력</span><span class="sxs-lookup"><span data-stu-id="c34ce-138">OUTPUTS</span></span>

### <span data-ttu-id="c34ce-139">Microsoft. KeyVault. \* ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c34ce-139">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="c34ce-140">상속자</span><span class="sxs-lookup"><span data-stu-id="c34ce-140">NOTES</span></span>

## <span data-ttu-id="c34ce-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c34ce-141">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

