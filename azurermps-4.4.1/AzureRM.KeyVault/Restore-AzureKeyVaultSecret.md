---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://go.microsoft.com/fwlink/?LinkId=690301
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
ms.openlocfilehash: bd619f6c4ec9891972d23738c1f2510cba0e2272
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703113"
---
# <span data-ttu-id="8bf33-101">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8bf33-101">Restore-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="8bf33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bf33-102">SYNOPSIS</span></span>
<span data-ttu-id="8bf33-103">백업 비밀의 키 보관소에 비밀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8bf33-103">Creates a secret in a key vault from a backed-up secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8bf33-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8bf33-104">SYNTAX</span></span>

```
Restore-AzureKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bf33-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8bf33-105">DESCRIPTION</span></span>
<span data-ttu-id="8bf33-106">**Restore-AzureKeyVaultSecret** cmdlet은 지정 된 키 보관소에 비밀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8bf33-106">The **Restore-AzureKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="8bf33-107">이 비밀은 입력 파일에 있는 백업 비밀의 복제본 이며, 원래 비밀 이름과 동일한 이름을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="8bf33-107">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="8bf33-108">키 자격 증명 모음에 같은 이름의 비밀이 이미 있는 경우 원래 비밀을 덮어쓰지 않고이 cmdlet이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bf33-108">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="8bf33-109">백업에 여러 버전의 비밀이 포함 되어 있으면 모든 버전이 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8bf33-109">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="8bf33-110">비밀을 복원 하는 키 보관소는 비밀을 백업한 키 보관소와 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8bf33-110">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="8bf33-111">그러나 키 자격 증명 모음이 동일한 구독을 사용 해야 하며 같은 지리 (예: 북미)의 Azure 지역에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bf33-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="8bf33-112"> https://azure.microsoft.com/support/trust-center/)Azure 지역을 지역에 매핑하는 Microsoft Azure 보안 센터를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8bf33-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="8bf33-113">예제의</span><span class="sxs-lookup"><span data-stu-id="8bf33-113">EXAMPLES</span></span>

### <span data-ttu-id="8bf33-114">예제 1: 백업 된 비밀 복원</span><span class="sxs-lookup"><span data-stu-id="8bf33-114">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzureKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="8bf33-115">이 명령은 모든 버전을 포함 한 비밀을 백업 파일 이름에서 MyKeyVault의 키 자격 증명 모음으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bf33-115">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="8bf33-116">변수</span><span class="sxs-lookup"><span data-stu-id="8bf33-116">PARAMETERS</span></span>

### <span data-ttu-id="8bf33-117">-InputFile</span><span class="sxs-lookup"><span data-stu-id="8bf33-117">-InputFile</span></span>
<span data-ttu-id="8bf33-118">복원할 비밀의 백업을 포함 하는 입력 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bf33-118">Specifies the input file that contains the backup of the secret to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bf33-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8bf33-119">-VaultName</span></span>
<span data-ttu-id="8bf33-120">비밀을 복원할 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bf33-120">Specifies the name of the key vault into which to restore the secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bf33-121">-확인</span><span class="sxs-lookup"><span data-stu-id="8bf33-121">-Confirm</span></span>
<span data-ttu-id="8bf33-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bf33-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bf33-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bf33-123">-WhatIf</span></span>
<span data-ttu-id="8bf33-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8bf33-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bf33-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8bf33-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bf33-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bf33-126">-DefaultProfile</span></span>
<span data-ttu-id="8bf33-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8bf33-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bf33-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bf33-128">CommonParameters</span></span>
<span data-ttu-id="8bf33-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bf33-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bf33-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bf33-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bf33-131">입력</span><span class="sxs-lookup"><span data-stu-id="8bf33-131">INPUTS</span></span>

## <span data-ttu-id="8bf33-132">출력</span><span class="sxs-lookup"><span data-stu-id="8bf33-132">OUTPUTS</span></span>

### <span data-ttu-id="8bf33-133">Microsoft. KeyVault. 모델 암호</span><span class="sxs-lookup"><span data-stu-id="8bf33-133">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="8bf33-134">상속자</span><span class="sxs-lookup"><span data-stu-id="8bf33-134">NOTES</span></span>

## <span data-ttu-id="8bf33-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8bf33-135">RELATED LINKS</span></span>

[<span data-ttu-id="8bf33-136">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8bf33-136">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="8bf33-137">백업-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8bf33-137">Backup-AzureKeyVaultSecret</span></span>](./Backup-AzureKeyVaultSecret.md)

[<span data-ttu-id="8bf33-138">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8bf33-138">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="8bf33-139">제거-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8bf33-139">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

