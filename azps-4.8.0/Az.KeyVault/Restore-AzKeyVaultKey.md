---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
ms.openlocfilehash: 17a39152c6e341773a2c3db7b701e0d37890f110
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211718"
---
# <span data-ttu-id="5edcf-101">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5edcf-101">Restore-AzKeyVaultKey</span></span>

## <span data-ttu-id="5edcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5edcf-102">SYNOPSIS</span></span>
<span data-ttu-id="5edcf-103">백업 키의 키 보관소에 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5edcf-103">Creates a key in a key vault from a backed-up key.</span></span>

## <span data-ttu-id="5edcf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5edcf-104">SYNTAX</span></span>

### <span data-ttu-id="5edcf-105">ByVaultName (기본값)</span><span class="sxs-lookup"><span data-stu-id="5edcf-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5edcf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5edcf-106">ByInputObject</span></span>
```
Restore-AzKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5edcf-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5edcf-107">ByResourceId</span></span>
```
Restore-AzKeyVaultKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5edcf-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5edcf-108">DESCRIPTION</span></span>
<span data-ttu-id="5edcf-109">**Restore-AzKeyVaultKey** cmdlet은 지정 된 키 보관소에 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5edcf-109">The **Restore-AzKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="5edcf-110">이 키는 입력 파일의 백업 키 복제본 이며 원래 키와 같은 이름을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="5edcf-110">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="5edcf-111">키 보관소에 같은 이름의 키가 이미 있는 경우, 원본 키를 덮어쓰지 않고이 cmdlet이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="5edcf-111">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="5edcf-112">백업에 여러 버전의 키가 포함 되어 있으면 모든 버전이 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5edcf-112">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="5edcf-113">키를 복원 하는 키 보관소는 해당 키를 백업한 키 보관소와 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5edcf-113">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="5edcf-114">그러나 키 자격 증명 모음이 동일한 구독을 사용 해야 하며 같은 지리 (예: 북미)의 Azure 지역에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5edcf-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="5edcf-115"> https://azure.microsoft.com/support/trust-center/)Azure 지역을 지역에 매핑하는 Microsoft Azure 보안 센터를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5edcf-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="5edcf-116">예제의</span><span class="sxs-lookup"><span data-stu-id="5edcf-116">EXAMPLES</span></span>

### <span data-ttu-id="5edcf-117">예제 1: 백업 된 키 복원</span><span class="sxs-lookup"><span data-stu-id="5edcf-117">Example 1: Restore a backed-up key</span></span>
```powershell
PS C:\> Restore-AzKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Vault Name     : MyKeyVault
Name           : key1
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://mykeyvault.vault.azure.net:443/keys/key1/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        :
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 4/6/2018 11:35:04 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="5edcf-118">이 명령은 모든 버전을 포함 한 키를 Backup. a y y (백업 파일 이름)에서 MyKeyVault 라는 키 자격 증명 모음으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5edcf-118">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="5edcf-119">변수</span><span class="sxs-lookup"><span data-stu-id="5edcf-119">PARAMETERS</span></span>

### <span data-ttu-id="5edcf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5edcf-120">-DefaultProfile</span></span>
<span data-ttu-id="5edcf-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5edcf-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5edcf-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="5edcf-122">-InputFile</span></span>
<span data-ttu-id="5edcf-123">복원할 키의 백업을 포함 하는 입력 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5edcf-123">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="5edcf-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5edcf-124">-InputObject</span></span>
<span data-ttu-id="5edcf-125">KeyVault 개체</span><span class="sxs-lookup"><span data-stu-id="5edcf-125">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5edcf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5edcf-126">-ResourceId</span></span>
<span data-ttu-id="5edcf-127">KeyVault 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="5edcf-127">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edcf-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5edcf-128">-VaultName</span></span>
<span data-ttu-id="5edcf-129">키를 복원할 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5edcf-129">Specifies the name of the key vault into which to restore the key.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5edcf-130">-확인</span><span class="sxs-lookup"><span data-stu-id="5edcf-130">-Confirm</span></span>
<span data-ttu-id="5edcf-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5edcf-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5edcf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5edcf-132">-WhatIf</span></span>
<span data-ttu-id="5edcf-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5edcf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5edcf-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5edcf-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5edcf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5edcf-135">CommonParameters</span></span>
<span data-ttu-id="5edcf-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5edcf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5edcf-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5edcf-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5edcf-138">입력</span><span class="sxs-lookup"><span data-stu-id="5edcf-138">INPUTS</span></span>

### <span data-ttu-id="5edcf-139">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="5edcf-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="5edcf-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5edcf-140">System.String</span></span>

## <span data-ttu-id="5edcf-141">출력</span><span class="sxs-lookup"><span data-stu-id="5edcf-141">OUTPUTS</span></span>

### <span data-ttu-id="5edcf-142">Microsoft. KeyVault. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5edcf-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="5edcf-143">상속자</span><span class="sxs-lookup"><span data-stu-id="5edcf-143">NOTES</span></span>

## <span data-ttu-id="5edcf-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5edcf-144">RELATED LINKS</span></span>

[<span data-ttu-id="5edcf-145">추가-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5edcf-145">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="5edcf-146">백업-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5edcf-146">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="5edcf-147">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5edcf-147">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="5edcf-148">제거-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5edcf-148">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

