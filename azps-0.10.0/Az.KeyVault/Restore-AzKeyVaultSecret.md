---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/restore-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
ms.openlocfilehash: 4691d37532db3dd8e629bf1daad2654558a31de3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876701"
---
# <span data-ttu-id="54ec3-101">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="54ec3-101">Restore-AzKeyVaultSecret</span></span>

## <span data-ttu-id="54ec3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54ec3-102">SYNOPSIS</span></span>
<span data-ttu-id="54ec3-103">백업 비밀의 키 보관소에 비밀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="54ec3-103">Creates a secret in a key vault from a backed-up secret.</span></span>

## <span data-ttu-id="54ec3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="54ec3-104">SYNTAX</span></span>

```
Restore-AzKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54ec3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="54ec3-105">DESCRIPTION</span></span>
<span data-ttu-id="54ec3-106">**Restore-AzKeyVaultSecret** cmdlet은 지정 된 키 보관소에 비밀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="54ec3-106">The **Restore-AzKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="54ec3-107">이 비밀은 입력 파일에 있는 백업 비밀의 복제본 이며, 원래 비밀 이름과 동일한 이름을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="54ec3-107">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="54ec3-108">키 자격 증명 모음에 같은 이름의 비밀이 이미 있는 경우 원래 비밀을 덮어쓰지 않고이 cmdlet이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="54ec3-108">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="54ec3-109">백업에 여러 버전의 비밀이 포함 되어 있으면 모든 버전이 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="54ec3-109">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="54ec3-110">비밀을 복원 하는 키 보관소는 비밀을 백업한 키 보관소와 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54ec3-110">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="54ec3-111">그러나 키 자격 증명 모음이 동일한 구독을 사용 해야 하며 같은 지리 (예: 북미)의 Azure 지역에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="54ec3-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="54ec3-112"> https://azure.microsoft.com/support/trust-center/)Azure 지역을 지역에 매핑하는 Microsoft Azure 보안 센터를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="54ec3-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="54ec3-113">예제의</span><span class="sxs-lookup"><span data-stu-id="54ec3-113">EXAMPLES</span></span>

### <span data-ttu-id="54ec3-114">예제 1: 백업 된 비밀 복원</span><span class="sxs-lookup"><span data-stu-id="54ec3-114">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="54ec3-115">이 명령은 모든 버전을 포함 한 비밀을 백업 파일 이름에서 MyKeyVault의 키 자격 증명 모음으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="54ec3-115">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="54ec3-116">변수</span><span class="sxs-lookup"><span data-stu-id="54ec3-116">PARAMETERS</span></span>

### <span data-ttu-id="54ec3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54ec3-117">-DefaultProfile</span></span>
<span data-ttu-id="54ec3-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="54ec3-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54ec3-119">-InputFile</span><span class="sxs-lookup"><span data-stu-id="54ec3-119">-InputFile</span></span>
<span data-ttu-id="54ec3-120">복원할 비밀의 백업을 포함 하는 입력 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54ec3-120">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="54ec3-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="54ec3-121">-VaultName</span></span>
<span data-ttu-id="54ec3-122">비밀을 복원할 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54ec3-122">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="54ec3-123">-확인</span><span class="sxs-lookup"><span data-stu-id="54ec3-123">-Confirm</span></span>
<span data-ttu-id="54ec3-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="54ec3-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54ec3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54ec3-125">-WhatIf</span></span>
<span data-ttu-id="54ec3-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="54ec3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54ec3-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="54ec3-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54ec3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54ec3-128">CommonParameters</span></span>
<span data-ttu-id="54ec3-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="54ec3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54ec3-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54ec3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54ec3-131">입력</span><span class="sxs-lookup"><span data-stu-id="54ec3-131">INPUTS</span></span>

### <span data-ttu-id="54ec3-132">않아야</span><span class="sxs-lookup"><span data-stu-id="54ec3-132">None</span></span>
<span data-ttu-id="54ec3-133">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="54ec3-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="54ec3-134">출력</span><span class="sxs-lookup"><span data-stu-id="54ec3-134">OUTPUTS</span></span>

### <span data-ttu-id="54ec3-135">Microsoft. KeyVault. 모델 암호</span><span class="sxs-lookup"><span data-stu-id="54ec3-135">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="54ec3-136">상속자</span><span class="sxs-lookup"><span data-stu-id="54ec3-136">NOTES</span></span>

## <span data-ttu-id="54ec3-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54ec3-137">RELATED LINKS</span></span>

[<span data-ttu-id="54ec3-138">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="54ec3-138">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="54ec3-139">백업-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="54ec3-139">Backup-AzKeyVaultSecret</span></span>](./Backup-AzKeyVaultSecret.md)

[<span data-ttu-id="54ec3-140">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="54ec3-140">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="54ec3-141">제거-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="54ec3-141">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

