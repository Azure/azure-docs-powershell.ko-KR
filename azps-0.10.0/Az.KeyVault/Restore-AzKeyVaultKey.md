---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/restore-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
ms.openlocfilehash: 5d090bae05e3d931fbf41b656ea66409d1297e8f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876704"
---
# <span data-ttu-id="5f674-101">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5f674-101">Restore-AzKeyVaultKey</span></span>

## <span data-ttu-id="5f674-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f674-102">SYNOPSIS</span></span>
<span data-ttu-id="5f674-103">백업 키의 키 보관소에 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5f674-103">Creates a key in a key vault from a backed-up key.</span></span>

## <span data-ttu-id="5f674-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5f674-104">SYNTAX</span></span>

```
Restore-AzKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f674-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5f674-105">DESCRIPTION</span></span>
<span data-ttu-id="5f674-106">**Restore-AzKeyVaultKey** cmdlet은 지정 된 키 보관소에 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5f674-106">The **Restore-AzKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="5f674-107">이 키는 입력 파일의 백업 키 복제본 이며 원래 키와 같은 이름을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="5f674-107">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="5f674-108">키 보관소에 같은 이름의 키가 이미 있는 경우, 원본 키를 덮어쓰지 않고이 cmdlet이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f674-108">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="5f674-109">백업에 여러 버전의 키가 포함 되어 있으면 모든 버전이 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5f674-109">If the backup contains multiple versions of a key, all versions are restored.</span></span>

<span data-ttu-id="5f674-110">키를 복원 하는 키 보관소는 해당 키를 백업한 키 보관소와 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5f674-110">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="5f674-111">그러나 키 자격 증명 모음이 동일한 구독을 사용 해야 하며 같은 지리 (예: 북미)의 Azure 지역에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f674-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="5f674-112"> https://azure.microsoft.com/support/trust-center/)Azure 지역을 지역에 매핑하는 Microsoft Azure 보안 센터를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5f674-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="5f674-113">예제의</span><span class="sxs-lookup"><span data-stu-id="5f674-113">EXAMPLES</span></span>

### <span data-ttu-id="5f674-114">예제 1: 백업 된 키 복원</span><span class="sxs-lookup"><span data-stu-id="5f674-114">Example 1: Restore a backed-up key</span></span>
```
PS C:\>Restore-AzKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="5f674-115">이 명령은 모든 버전을 포함 한 키를 Backup. a y y (백업 파일 이름)에서 MyKeyVault 라는 키 자격 증명 모음으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f674-115">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="5f674-116">변수</span><span class="sxs-lookup"><span data-stu-id="5f674-116">PARAMETERS</span></span>

### <span data-ttu-id="5f674-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f674-117">-DefaultProfile</span></span>
<span data-ttu-id="5f674-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5f674-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f674-119">-InputFile</span><span class="sxs-lookup"><span data-stu-id="5f674-119">-InputFile</span></span>
<span data-ttu-id="5f674-120">복원할 키의 백업을 포함 하는 입력 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f674-120">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="5f674-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5f674-121">-VaultName</span></span>
<span data-ttu-id="5f674-122">키를 복원할 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f674-122">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="5f674-123">-확인</span><span class="sxs-lookup"><span data-stu-id="5f674-123">-Confirm</span></span>
<span data-ttu-id="5f674-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f674-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f674-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f674-125">-WhatIf</span></span>
<span data-ttu-id="5f674-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5f674-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f674-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5f674-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f674-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f674-128">CommonParameters</span></span>
<span data-ttu-id="5f674-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f674-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f674-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f674-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f674-131">입력</span><span class="sxs-lookup"><span data-stu-id="5f674-131">INPUTS</span></span>

### <span data-ttu-id="5f674-132">않아야</span><span class="sxs-lookup"><span data-stu-id="5f674-132">None</span></span>
<span data-ttu-id="5f674-133">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5f674-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5f674-134">출력</span><span class="sxs-lookup"><span data-stu-id="5f674-134">OUTPUTS</span></span>

### <span data-ttu-id="5f674-135">Microsoft. KeyVault. Keyvault</span><span class="sxs-lookup"><span data-stu-id="5f674-135">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="5f674-136">상속자</span><span class="sxs-lookup"><span data-stu-id="5f674-136">NOTES</span></span>

## <span data-ttu-id="5f674-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f674-137">RELATED LINKS</span></span>

[<span data-ttu-id="5f674-138">추가-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5f674-138">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="5f674-139">백업-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5f674-139">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="5f674-140">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5f674-140">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="5f674-141">제거-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5f674-141">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

