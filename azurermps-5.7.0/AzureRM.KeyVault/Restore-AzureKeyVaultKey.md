---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
ms.openlocfilehash: aee61173ee327d0c65f4cc04451fd64f51a79522
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702854"
---
# <span data-ttu-id="e2356-101">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e2356-101">Restore-AzureKeyVaultKey</span></span>

## <span data-ttu-id="e2356-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2356-102">SYNOPSIS</span></span>
<span data-ttu-id="e2356-103">백업 키의 키 보관소에 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e2356-103">Creates a key in a key vault from a backed-up key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2356-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e2356-104">SYNTAX</span></span>

### <span data-ttu-id="e2356-105">ByVaultName (기본값)</span><span class="sxs-lookup"><span data-stu-id="e2356-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2356-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e2356-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2356-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e2356-107">DESCRIPTION</span></span>
<span data-ttu-id="e2356-108">**Restore-AzureKeyVaultKey** cmdlet은 지정 된 키 보관소에 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e2356-108">The **Restore-AzureKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="e2356-109">이 키는 입력 파일의 백업 키 복제본 이며 원래 키와 같은 이름을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="e2356-109">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="e2356-110">키 보관소에 같은 이름의 키가 이미 있는 경우, 원본 키를 덮어쓰지 않고이 cmdlet이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2356-110">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="e2356-111">백업에 여러 버전의 키가 포함 되어 있으면 모든 버전이 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2356-111">If the backup contains multiple versions of a key, all versions are restored.</span></span>

<span data-ttu-id="e2356-112">키를 복원 하는 키 보관소는 해당 키를 백업한 키 보관소와 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2356-112">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="e2356-113">그러나 키 자격 증명 모음이 동일한 구독을 사용 해야 하며 같은 지리 (예: 북미)의 Azure 지역에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2356-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="e2356-114"> https://azure.microsoft.com/support/trust-center/)Azure 지역을 지역에 매핑하는 Microsoft Azure 보안 센터를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e2356-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="e2356-115">예제의</span><span class="sxs-lookup"><span data-stu-id="e2356-115">EXAMPLES</span></span>

### <span data-ttu-id="e2356-116">예제 1: 백업 된 키 복원</span><span class="sxs-lookup"><span data-stu-id="e2356-116">Example 1: Restore a backed-up key</span></span>
```
PS C:\>Restore-AzureKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="e2356-117">이 명령은 모든 버전을 포함 한 키를 Backup. a y y (백업 파일 이름)에서 MyKeyVault 라는 키 자격 증명 모음으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2356-117">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="e2356-118">변수</span><span class="sxs-lookup"><span data-stu-id="e2356-118">PARAMETERS</span></span>

### <span data-ttu-id="e2356-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2356-119">-DefaultProfile</span></span>
<span data-ttu-id="e2356-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e2356-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2356-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="e2356-121">-InputFile</span></span>
<span data-ttu-id="e2356-122">복원할 키의 백업을 포함 하는 입력 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2356-122">Specifies the input file that contains the backup of the key to restore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2356-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2356-123">-InputObject</span></span>
<span data-ttu-id="e2356-124">KeyVault 개체</span><span class="sxs-lookup"><span data-stu-id="e2356-124">KeyVault object</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2356-125">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e2356-125">-VaultName</span></span>
<span data-ttu-id="e2356-126">키를 복원할 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2356-126">Specifies the name of the key vault into which to restore the key.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2356-127">-확인</span><span class="sxs-lookup"><span data-stu-id="e2356-127">-Confirm</span></span>
<span data-ttu-id="e2356-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2356-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2356-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2356-129">-WhatIf</span></span>
<span data-ttu-id="e2356-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e2356-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2356-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2356-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2356-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2356-132">CommonParameters</span></span>
<span data-ttu-id="e2356-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2356-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2356-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2356-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2356-135">입력</span><span class="sxs-lookup"><span data-stu-id="e2356-135">INPUTS</span></span>

### <span data-ttu-id="e2356-136">않아야</span><span class="sxs-lookup"><span data-stu-id="e2356-136">None</span></span>
<span data-ttu-id="e2356-137">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2356-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e2356-138">출력</span><span class="sxs-lookup"><span data-stu-id="e2356-138">OUTPUTS</span></span>

### <span data-ttu-id="e2356-139">Microsoft. KeyVault. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e2356-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="e2356-140">상속자</span><span class="sxs-lookup"><span data-stu-id="e2356-140">NOTES</span></span>

## <span data-ttu-id="e2356-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2356-141">RELATED LINKS</span></span>

[<span data-ttu-id="e2356-142">추가-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e2356-142">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="e2356-143">백업-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e2356-143">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="e2356-144">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e2356-144">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="e2356-145">제거-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e2356-145">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

