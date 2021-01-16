---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
ms.openlocfilehash: 885be17315e0dc0be8223f0d28bc11a6d6e41146
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334377"
---
# <span data-ttu-id="e2368-101">Update-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="e2368-101">Update-AzSqlVMGroup</span></span>

## <span data-ttu-id="e2368-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2368-102">SYNOPSIS</span></span>
<span data-ttu-id="e2368-103">SQL 가상 머신 그룹을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e2368-103">Updates a sql virtual machine group.</span></span>

## <span data-ttu-id="e2368-104">구문</span><span class="sxs-lookup"><span data-stu-id="e2368-104">SYNTAX</span></span>

### <span data-ttu-id="e2368-105">이름(기본값)</span><span class="sxs-lookup"><span data-stu-id="e2368-105">Name (Default)</span></span>
```
Update-AzSqlVMGroup [-AsJob] [-ClusterOperatorAccount <String>] [-SqlServiceAccount <String>]
 [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>] [-DomainFqdn <String>]
 [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2368-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e2368-106">InputObject</span></span>
```
Update-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2368-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2368-107">ResourceId</span></span>
```
Update-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2368-108">설명</span><span class="sxs-lookup"><span data-stu-id="e2368-108">DESCRIPTION</span></span>
<span data-ttu-id="e2368-109">Update-AzSqlVMGroup cmdlet은 SQL 가상 머신 그룹을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e2368-109">The Update-AzSqlVMGroup cmdlet updates a sql virtual machine group.</span></span>

## <span data-ttu-id="e2368-110">예제</span><span class="sxs-lookup"><span data-stu-id="e2368-110">EXAMPLES</span></span>

### <span data-ttu-id="e2368-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e2368-111">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $group = Update-AzSqlVMGroup -InputObject $group -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="e2368-112">SQL 가상 머신 그룹의 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e2368-112">Updates the tags of a sql virtual machine group.</span></span>

## <span data-ttu-id="e2368-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2368-113">PARAMETERS</span></span>

### <span data-ttu-id="e2368-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2368-114">-AsJob</span></span>
<span data-ttu-id="e2368-115">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e2368-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="e2368-116">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="e2368-116">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="e2368-117">클러스터를 만드는 데 사용되는 이름</span><span class="sxs-lookup"><span data-stu-id="e2368-117">Name used for creating cluster</span></span>

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

### <span data-ttu-id="e2368-118">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="e2368-118">-ClusterOperatorAccount</span></span>
<span data-ttu-id="e2368-119">클러스터 운영에 사용되는 이름</span><span class="sxs-lookup"><span data-stu-id="e2368-119">Name used for operating cluster</span></span>

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

### <span data-ttu-id="e2368-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2368-120">-DefaultProfile</span></span>
<span data-ttu-id="e2368-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2368-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2368-122">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="e2368-122">-DomainFqdn</span></span>
<span data-ttu-id="e2368-123">도메인의 정식 이름</span><span class="sxs-lookup"><span data-stu-id="e2368-123">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="e2368-124">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="e2368-124">-FileShareWitnessPath</span></span>
<span data-ttu-id="e2368-125">파일 공유 미러링 미러링에 대한 선택적 경로</span><span class="sxs-lookup"><span data-stu-id="e2368-125">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="e2368-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2368-126">-InputObject</span></span>
<span data-ttu-id="e2368-127">SQL 가상 머신 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e2368-127">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="e2368-128">-Name</span><span class="sxs-lookup"><span data-stu-id="e2368-128">-Name</span></span>
<span data-ttu-id="e2368-129">SQL 컴퓨터 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2368-129">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="e2368-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="e2368-130">-OuPath</span></span>
<span data-ttu-id="e2368-131">노드 및 클러스터가 있는 조직 구성 단위 경로</span><span class="sxs-lookup"><span data-stu-id="e2368-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="e2368-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2368-132">-ResourceGroupName</span></span>
<span data-ttu-id="e2368-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2368-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="e2368-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2368-134">-ResourceId</span></span>
<span data-ttu-id="e2368-135">SQL 컴퓨터 그룹 리소스 ID를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e2368-135">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="e2368-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="e2368-136">-SqlServiceAccount</span></span>
<span data-ttu-id="e2368-137">클러스터의 모든 SQL 가상 머신에서 SQL 서비스에서 실행되는 이름</span><span class="sxs-lookup"><span data-stu-id="e2368-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="e2368-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="e2368-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="e2368-139">미러링 저장소 계정의 기본 키</span><span class="sxs-lookup"><span data-stu-id="e2368-139">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="e2368-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="e2368-140">-StorageAccountUrl</span></span>
<span data-ttu-id="e2368-141">미러링 저장소 계정의 기본 키</span><span class="sxs-lookup"><span data-stu-id="e2368-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="e2368-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="e2368-142">-Tag</span></span>
<span data-ttu-id="e2368-143">가상 머신 그룹과 SQL 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="e2368-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="e2368-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2368-144">-Confirm</span></span>
<span data-ttu-id="e2368-145">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2368-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2368-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2368-146">-WhatIf</span></span>
<span data-ttu-id="e2368-147">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e2368-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2368-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2368-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2368-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2368-149">CommonParameters</span></span>
<span data-ttu-id="e2368-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e2368-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2368-151">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e2368-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2368-152">입력</span><span class="sxs-lookup"><span data-stu-id="e2368-152">INPUTS</span></span>

### <span data-ttu-id="e2368-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="e2368-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="e2368-154">System.String</span><span class="sxs-lookup"><span data-stu-id="e2368-154">System.String</span></span>

## <span data-ttu-id="e2368-155">출력</span><span class="sxs-lookup"><span data-stu-id="e2368-155">OUTPUTS</span></span>

### <span data-ttu-id="e2368-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="e2368-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="e2368-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e2368-157">NOTES</span></span>

## <span data-ttu-id="e2368-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2368-158">RELATED LINKS</span></span>
