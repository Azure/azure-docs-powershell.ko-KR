---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: a62e6093ec5cfdf7244ea83b2dccf07ad07308fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968320"
---
# <span data-ttu-id="68969-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="68969-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="68969-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68969-102">SYNOPSIS</span></span>
<span data-ttu-id="68969-103">ANF(Azure NetApp Files) 풀을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="68969-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="68969-104">구문</span><span class="sxs-lookup"><span data-stu-id="68969-104">SYNTAX</span></span>

### <span data-ttu-id="68969-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="68969-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68969-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68969-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68969-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68969-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68969-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68969-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68969-109">설명</span><span class="sxs-lookup"><span data-stu-id="68969-109">DESCRIPTION</span></span>
<span data-ttu-id="68969-110">**Remove-AzNetAppFilesPool** cmdlet은 ANF 풀을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="68969-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="68969-111">예제</span><span class="sxs-lookup"><span data-stu-id="68969-111">EXAMPLES</span></span>

### <span data-ttu-id="68969-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="68969-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="68969-113">이 명령은 ANF 풀 "MyAnfPool"을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="68969-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="68969-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="68969-114">PARAMETERS</span></span>

### <span data-ttu-id="68969-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="68969-115">-AccountName</span></span>
<span data-ttu-id="68969-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="68969-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68969-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="68969-117">-AccountObject</span></span>
<span data-ttu-id="68969-118">제거할 풀이 포함된 계정 개체</span><span class="sxs-lookup"><span data-stu-id="68969-118">The account object containing the pool to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68969-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68969-119">-DefaultProfile</span></span>
<span data-ttu-id="68969-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68969-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68969-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68969-121">-InputObject</span></span>
<span data-ttu-id="68969-122">제거할 풀 개체</span><span class="sxs-lookup"><span data-stu-id="68969-122">The pool object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68969-123">-Name</span><span class="sxs-lookup"><span data-stu-id="68969-123">-Name</span></span>
<span data-ttu-id="68969-124">ANF 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="68969-124">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68969-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68969-125">-PassThru</span></span>
<span data-ttu-id="68969-126">지정된 풀이 성공적으로 제거된지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="68969-126">Return whether the specified pool was successfully removed</span></span>

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

### <span data-ttu-id="68969-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68969-127">-ResourceGroupName</span></span>
<span data-ttu-id="68969-128">ANF 풀의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="68969-128">The resource group of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68969-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68969-129">-ResourceId</span></span>
<span data-ttu-id="68969-130">ANF 풀의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="68969-130">The resource id of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68969-131">-확인</span><span class="sxs-lookup"><span data-stu-id="68969-131">-Confirm</span></span>
<span data-ttu-id="68969-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="68969-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68969-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68969-133">-WhatIf</span></span>
<span data-ttu-id="68969-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="68969-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68969-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68969-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68969-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68969-136">CommonParameters</span></span>
<span data-ttu-id="68969-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="68969-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68969-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68969-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68969-139">입력</span><span class="sxs-lookup"><span data-stu-id="68969-139">INPUTS</span></span>

### <span data-ttu-id="68969-140">System.String</span><span class="sxs-lookup"><span data-stu-id="68969-140">System.String</span></span>

### <span data-ttu-id="68969-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="68969-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="68969-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="68969-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="68969-143">출력</span><span class="sxs-lookup"><span data-stu-id="68969-143">OUTPUTS</span></span>

### <span data-ttu-id="68969-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="68969-144">System.Boolean</span></span>

## <span data-ttu-id="68969-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="68969-145">NOTES</span></span>

## <span data-ttu-id="68969-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68969-146">RELATED LINKS</span></span>
