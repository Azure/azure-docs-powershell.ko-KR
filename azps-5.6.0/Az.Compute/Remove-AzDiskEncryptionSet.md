---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
ms.openlocfilehash: ec146441e620580b5028dffa4e0f7f3e09c45b35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988367"
---
# <span data-ttu-id="e764f-101">Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="e764f-101">Remove-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="e764f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e764f-102">SYNOPSIS</span></span>
<span data-ttu-id="e764f-103">디스크 암호화 집합을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e764f-103">Removes a disk encryption set.</span></span>

## <span data-ttu-id="e764f-104">구문</span><span class="sxs-lookup"><span data-stu-id="e764f-104">SYNTAX</span></span>

### <span data-ttu-id="e764f-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="e764f-105">DefaultParameter (Default)</span></span>
```
Remove-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e764f-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="e764f-106">ResourceIdParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e764f-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="e764f-107">ObjectParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-InputObject] <PSDiskEncryptionSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e764f-108">설명</span><span class="sxs-lookup"><span data-stu-id="e764f-108">DESCRIPTION</span></span>
<span data-ttu-id="e764f-109">디스크 암호화 집합을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e764f-109">Removes a disk encryption set.</span></span>

## <span data-ttu-id="e764f-110">예제</span><span class="sxs-lookup"><span data-stu-id="e764f-110">EXAMPLES</span></span>

### <span data-ttu-id="e764f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e764f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -Force;
```

<span data-ttu-id="e764f-112">'rg1'에서 디스크 암호화 집합 'enc1' 삭제</span><span class="sxs-lookup"><span data-stu-id="e764f-112">Delete disk encryption set 'enc1' in 'rg1'</span></span>

## <span data-ttu-id="e764f-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e764f-113">PARAMETERS</span></span>

### <span data-ttu-id="e764f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e764f-114">-AsJob</span></span>
<span data-ttu-id="e764f-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e764f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e764f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e764f-116">-DefaultProfile</span></span>
<span data-ttu-id="e764f-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e764f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e764f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e764f-118">-Force</span></span>
<span data-ttu-id="e764f-119">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e764f-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e764f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e764f-120">-InputObject</span></span>
<span data-ttu-id="e764f-121">디스크 암호화 집합의 로컬 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e764f-121">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="e764f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e764f-122">-Name</span></span>
<span data-ttu-id="e764f-123">디스크 암호화 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e764f-123">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="e764f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e764f-124">-ResourceGroupName</span></span>
<span data-ttu-id="e764f-125">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e764f-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e764f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e764f-126">-ResourceId</span></span>
<span data-ttu-id="e764f-127">리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e764f-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="e764f-128">-확인</span><span class="sxs-lookup"><span data-stu-id="e764f-128">-Confirm</span></span>
<span data-ttu-id="e764f-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e764f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e764f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e764f-130">-WhatIf</span></span>
<span data-ttu-id="e764f-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e764f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e764f-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e764f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e764f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e764f-133">CommonParameters</span></span>
<span data-ttu-id="e764f-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e764f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e764f-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e764f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e764f-136">입력</span><span class="sxs-lookup"><span data-stu-id="e764f-136">INPUTS</span></span>

### <span data-ttu-id="e764f-137">System.String</span><span class="sxs-lookup"><span data-stu-id="e764f-137">System.String</span></span>

### <span data-ttu-id="e764f-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="e764f-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="e764f-139">출력</span><span class="sxs-lookup"><span data-stu-id="e764f-139">OUTPUTS</span></span>

### <span data-ttu-id="e764f-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="e764f-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="e764f-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e764f-141">NOTES</span></span>

## <span data-ttu-id="e764f-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e764f-142">RELATED LINKS</span></span>
