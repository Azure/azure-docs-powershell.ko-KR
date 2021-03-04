---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/update-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
ms.openlocfilehash: 04a75ec50f985bb1cea0266c077946adbdab4f65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999231"
---
# <span data-ttu-id="24577-101">Update-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="24577-101">Update-AzSqlVMGroup</span></span>

## <span data-ttu-id="24577-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24577-102">SYNOPSIS</span></span>
<span data-ttu-id="24577-103">SQL 가상 머신 그룹을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="24577-103">Updates a sql virtual machine group.</span></span>

## <span data-ttu-id="24577-104">구문</span><span class="sxs-lookup"><span data-stu-id="24577-104">SYNTAX</span></span>

### <span data-ttu-id="24577-105">이름(기본값)</span><span class="sxs-lookup"><span data-stu-id="24577-105">Name (Default)</span></span>
```
Update-AzSqlVMGroup [-AsJob] [-ClusterOperatorAccount <String>] [-SqlServiceAccount <String>]
 [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>] [-DomainFqdn <String>]
 [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24577-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="24577-106">InputObject</span></span>
```
Update-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24577-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="24577-107">ResourceId</span></span>
```
Update-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24577-108">설명</span><span class="sxs-lookup"><span data-stu-id="24577-108">DESCRIPTION</span></span>
<span data-ttu-id="24577-109">Update-AzSqlVMGroup cmdlet은 SQL 가상 머신 그룹을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="24577-109">The Update-AzSqlVMGroup cmdlet updates a sql virtual machine group.</span></span>

## <span data-ttu-id="24577-110">예제</span><span class="sxs-lookup"><span data-stu-id="24577-110">EXAMPLES</span></span>

### <span data-ttu-id="24577-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="24577-111">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $group = Update-AzSqlVMGroup -InputObject $group -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="24577-112">SQL 가상 머신 그룹의 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="24577-112">Updates the tags of a sql virtual machine group.</span></span>

## <span data-ttu-id="24577-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="24577-113">PARAMETERS</span></span>

### <span data-ttu-id="24577-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24577-114">-AsJob</span></span>
<span data-ttu-id="24577-115">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="24577-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="24577-116">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="24577-116">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="24577-117">클러스터를 만드는 데 사용되는 이름</span><span class="sxs-lookup"><span data-stu-id="24577-117">Name used for creating cluster</span></span>

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

### <span data-ttu-id="24577-118">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="24577-118">-ClusterOperatorAccount</span></span>
<span data-ttu-id="24577-119">클러스터 운영에 사용되는 이름</span><span class="sxs-lookup"><span data-stu-id="24577-119">Name used for operating cluster</span></span>

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

### <span data-ttu-id="24577-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24577-120">-DefaultProfile</span></span>
<span data-ttu-id="24577-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24577-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24577-122">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="24577-122">-DomainFqdn</span></span>
<span data-ttu-id="24577-123">도메인의 완전 자격을 갖춘 이름</span><span class="sxs-lookup"><span data-stu-id="24577-123">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="24577-124">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="24577-124">-FileShareWitnessPath</span></span>
<span data-ttu-id="24577-125">파일 공유 증인에 대한 선택적 경로</span><span class="sxs-lookup"><span data-stu-id="24577-125">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="24577-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24577-126">-InputObject</span></span>
<span data-ttu-id="24577-127">SQL 가상 머신 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="24577-127">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: InputObject
Aliases: SqlVMGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24577-128">-Name</span><span class="sxs-lookup"><span data-stu-id="24577-128">-Name</span></span>
<span data-ttu-id="24577-129">SQL 컴퓨터 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="24577-129">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24577-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="24577-130">-OuPath</span></span>
<span data-ttu-id="24577-131">노드 및 클러스터가 있는 조직 단위 경로</span><span class="sxs-lookup"><span data-stu-id="24577-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="24577-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24577-132">-ResourceGroupName</span></span>
<span data-ttu-id="24577-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24577-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24577-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24577-134">-ResourceId</span></span>
<span data-ttu-id="24577-135">SQL 그룹 리소스 ID를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="24577-135">SQL virtual machine group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24577-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="24577-136">-SqlServiceAccount</span></span>
<span data-ttu-id="24577-137">클러스터의 SQL 참여하는 모든 가상 머신에서 SQL 실행되는 이름</span><span class="sxs-lookup"><span data-stu-id="24577-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="24577-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="24577-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="24577-139">미러링 저장소 계정의 기본 키</span><span class="sxs-lookup"><span data-stu-id="24577-139">Primary key of the witness storage account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24577-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="24577-140">-StorageAccountUrl</span></span>
<span data-ttu-id="24577-141">미러링 저장소 계정의 기본 키</span><span class="sxs-lookup"><span data-stu-id="24577-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="24577-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="24577-142">-Tag</span></span>
<span data-ttu-id="24577-143">가상 머신 그룹과 SQL 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="24577-143">The tags to associate with the SQL virtual machine group.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24577-144">-확인</span><span class="sxs-lookup"><span data-stu-id="24577-144">-Confirm</span></span>
<span data-ttu-id="24577-145">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="24577-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24577-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24577-146">-WhatIf</span></span>
<span data-ttu-id="24577-147">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="24577-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24577-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24577-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24577-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24577-149">CommonParameters</span></span>
<span data-ttu-id="24577-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="24577-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24577-151">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24577-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24577-152">입력</span><span class="sxs-lookup"><span data-stu-id="24577-152">INPUTS</span></span>

### <span data-ttu-id="24577-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="24577-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="24577-154">System.String</span><span class="sxs-lookup"><span data-stu-id="24577-154">System.String</span></span>

## <span data-ttu-id="24577-155">출력</span><span class="sxs-lookup"><span data-stu-id="24577-155">OUTPUTS</span></span>

### <span data-ttu-id="24577-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="24577-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="24577-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="24577-157">NOTES</span></span>

## <span data-ttu-id="24577-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24577-158">RELATED LINKS</span></span>
