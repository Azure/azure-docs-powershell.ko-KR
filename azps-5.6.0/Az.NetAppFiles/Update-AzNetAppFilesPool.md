---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: e8b367b724a4310eb5a3ed76bcf02e8538299845
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968112"
---
# <span data-ttu-id="eecd3-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="eecd3-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="eecd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eecd3-102">SYNOPSIS</span></span>
<span data-ttu-id="eecd3-103">제공된 선택적 수정자에 따라 ANF(Azure NetApp Files) 풀을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="eecd3-103">Updates an Azure NetApp Files (ANF) pool according to the optional modifiers provided.</span></span>

## <span data-ttu-id="eecd3-104">구문</span><span class="sxs-lookup"><span data-stu-id="eecd3-104">SYNTAX</span></span>

### <span data-ttu-id="eecd3-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="eecd3-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> [-Location <String>] -AccountName <String> -Name <String>
 [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eecd3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eecd3-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eecd3-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eecd3-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eecd3-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eecd3-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eecd3-109">설명</span><span class="sxs-lookup"><span data-stu-id="eecd3-109">DESCRIPTION</span></span>
<span data-ttu-id="eecd3-110">**Update-AzNetAppFilesPool** cmdlet은 ANF 풀을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="eecd3-110">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="eecd3-111">예제</span><span class="sxs-lookup"><span data-stu-id="eecd3-111">EXAMPLES</span></span>

### <span data-ttu-id="eecd3-112">예제 1: ANF 풀 수정</span><span class="sxs-lookup"><span data-stu-id="eecd3-112">Example 1: Modify an ANF pool</span></span>
```
PS C:\>Update-AzNetAppFilesPool -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolSize 4398046511104 -QosType "Auto"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
Size              : 4398046511104
ServiceLevel      : Standard
QosType           : Auto
ProvisioningState : Succeeded
```

<span data-ttu-id="eecd3-113">이 명령은 ANF 풀 "MyAnfPool"을 주어진 크기와 QosType로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="eecd3-113">This command changes the ANF pool "MyAnfPool" to have the given size and QosType.</span></span>

## <span data-ttu-id="eecd3-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="eecd3-114">PARAMETERS</span></span>

### <span data-ttu-id="eecd3-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eecd3-115">-AccountName</span></span>
<span data-ttu-id="eecd3-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="eecd3-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="eecd3-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="eecd3-117">-AccountObject</span></span>
<span data-ttu-id="eecd3-118">업데이트할 풀이 포함된 계정 개체</span><span class="sxs-lookup"><span data-stu-id="eecd3-118">The account object containing the pool to update</span></span>

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

### <span data-ttu-id="eecd3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eecd3-119">-DefaultProfile</span></span>
<span data-ttu-id="eecd3-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eecd3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eecd3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eecd3-121">-InputObject</span></span>
<span data-ttu-id="eecd3-122">업데이트할 풀 개체</span><span class="sxs-lookup"><span data-stu-id="eecd3-122">The pool object to update</span></span>

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

### <span data-ttu-id="eecd3-123">-Location</span><span class="sxs-lookup"><span data-stu-id="eecd3-123">-Location</span></span>
<span data-ttu-id="eecd3-124">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="eecd3-124">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eecd3-125">-Name</span><span class="sxs-lookup"><span data-stu-id="eecd3-125">-Name</span></span>
<span data-ttu-id="eecd3-126">ANF 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="eecd3-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="eecd3-127">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="eecd3-127">-PoolSize</span></span>
<span data-ttu-id="eecd3-128">ANF 풀의 크기</span><span class="sxs-lookup"><span data-stu-id="eecd3-128">The size of the ANF pool</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eecd3-129">-QosType</span><span class="sxs-lookup"><span data-stu-id="eecd3-129">-QosType</span></span>
<span data-ttu-id="eecd3-130">풀의 qos 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="eecd3-130">The qos type of the pool.</span></span> <span data-ttu-id="eecd3-131">가능한 값은 다음과 같습니다. '자동', '수동'</span><span class="sxs-lookup"><span data-stu-id="eecd3-131">Possible values include: 'Auto', 'Manual'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eecd3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eecd3-132">-ResourceGroupName</span></span>
<span data-ttu-id="eecd3-133">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="eecd3-133">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="eecd3-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eecd3-134">-ResourceId</span></span>
<span data-ttu-id="eecd3-135">ANF 풀의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="eecd3-135">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="eecd3-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="eecd3-136">-Tag</span></span>
<span data-ttu-id="eecd3-137">리소스 태그를 나타내는 해시테이블</span><span class="sxs-lookup"><span data-stu-id="eecd3-137">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eecd3-138">-확인</span><span class="sxs-lookup"><span data-stu-id="eecd3-138">-Confirm</span></span>
<span data-ttu-id="eecd3-139">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="eecd3-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eecd3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eecd3-140">-WhatIf</span></span>
<span data-ttu-id="eecd3-141">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="eecd3-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eecd3-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eecd3-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eecd3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eecd3-143">CommonParameters</span></span>
<span data-ttu-id="eecd3-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eecd3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eecd3-145">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eecd3-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eecd3-146">입력</span><span class="sxs-lookup"><span data-stu-id="eecd3-146">INPUTS</span></span>

### <span data-ttu-id="eecd3-147">System.String</span><span class="sxs-lookup"><span data-stu-id="eecd3-147">System.String</span></span>

### <span data-ttu-id="eecd3-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="eecd3-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="eecd3-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="eecd3-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="eecd3-150">출력</span><span class="sxs-lookup"><span data-stu-id="eecd3-150">OUTPUTS</span></span>

### <span data-ttu-id="eecd3-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="eecd3-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="eecd3-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="eecd3-152">NOTES</span></span>

## <span data-ttu-id="eecd3-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eecd3-153">RELATED LINKS</span></span>
