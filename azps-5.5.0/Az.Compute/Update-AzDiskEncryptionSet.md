---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
ms.openlocfilehash: 0e95179dcd2b1948b55526f3f2a8bfd5bb1a8834
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177404"
---
# <span data-ttu-id="f2dae-101">Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="f2dae-101">Update-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="f2dae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2dae-102">SYNOPSIS</span></span>
<span data-ttu-id="f2dae-103">디스크 암호화 집합을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f2dae-103">Updates a disk encryption set.</span></span>

## <span data-ttu-id="f2dae-104">구문</span><span class="sxs-lookup"><span data-stu-id="f2dae-104">SYNTAX</span></span>

### <span data-ttu-id="f2dae-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="f2dae-105">DefaultParameter (Default)</span></span>
```
Update-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-KeyUrl <String>]
 [-SourceVaultId <String>] [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2dae-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="f2dae-106">ResourceIdParameter</span></span>
```
Update-AzDiskEncryptionSet [-ResourceId] <String> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2dae-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="f2dae-107">ObjectParameter</span></span>
```
Update-AzDiskEncryptionSet [-InputObject] <PSDiskEncryptionSet> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2dae-108">설명</span><span class="sxs-lookup"><span data-stu-id="f2dae-108">DESCRIPTION</span></span>
<span data-ttu-id="f2dae-109">디스크 암호화 집합을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f2dae-109">Updates a disk encryption set.</span></span>

## <span data-ttu-id="f2dae-110">예제</span><span class="sxs-lookup"><span data-stu-id="f2dae-110">EXAMPLES</span></span>

### <span data-ttu-id="f2dae-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f2dae-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1;
```

<span data-ttu-id="f2dae-112">키 자격 증명 모음에서 제공된 활성 키를 사용하여 디스크 암호화 집합을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f2dae-112">Updates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="f2dae-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2dae-113">PARAMETERS</span></span>

### <span data-ttu-id="f2dae-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2dae-114">-AsJob</span></span>
<span data-ttu-id="f2dae-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f2dae-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2dae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2dae-116">-DefaultProfile</span></span>
<span data-ttu-id="f2dae-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f2dae-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2dae-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2dae-118">-InputObject</span></span>
<span data-ttu-id="f2dae-119">디스크 암호화 집합의 로컬 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f2dae-119">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: ObjectParameter
Aliases: DiskEncryptionSet

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2dae-120">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="f2dae-120">-KeyUrl</span></span>
<span data-ttu-id="f2dae-121">KeyVault에서 활성 키를 참조하는 URL</span><span class="sxs-lookup"><span data-stu-id="f2dae-121">Url pointing to the active key in KeyVault</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2dae-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f2dae-122">-Name</span></span>
<span data-ttu-id="f2dae-123">디스크 암호화 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f2dae-123">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2dae-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2dae-124">-ResourceGroupName</span></span>
<span data-ttu-id="f2dae-125">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f2dae-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2dae-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2dae-126">-ResourceId</span></span>
<span data-ttu-id="f2dae-127">리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f2dae-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2dae-128">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="f2dae-128">-SourceVaultId</span></span>
<span data-ttu-id="f2dae-129">활성 키를 포함하는 KeyVault의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f2dae-129">Resource id of the KeyVault containing the active key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2dae-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="f2dae-130">-Tag</span></span>
<span data-ttu-id="f2dae-131">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="f2dae-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f2dae-132">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="f2dae-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2dae-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2dae-133">-Confirm</span></span>
<span data-ttu-id="f2dae-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2dae-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2dae-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2dae-135">-WhatIf</span></span>
<span data-ttu-id="f2dae-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f2dae-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2dae-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2dae-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2dae-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2dae-138">CommonParameters</span></span>
<span data-ttu-id="f2dae-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f2dae-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2dae-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f2dae-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2dae-141">입력</span><span class="sxs-lookup"><span data-stu-id="f2dae-141">INPUTS</span></span>

### <span data-ttu-id="f2dae-142">System.String</span><span class="sxs-lookup"><span data-stu-id="f2dae-142">System.String</span></span>

### <span data-ttu-id="f2dae-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="f2dae-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

### <span data-ttu-id="f2dae-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f2dae-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f2dae-145">출력</span><span class="sxs-lookup"><span data-stu-id="f2dae-145">OUTPUTS</span></span>

### <span data-ttu-id="f2dae-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="f2dae-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="f2dae-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f2dae-147">NOTES</span></span>

## <span data-ttu-id="f2dae-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2dae-148">RELATED LINKS</span></span>
