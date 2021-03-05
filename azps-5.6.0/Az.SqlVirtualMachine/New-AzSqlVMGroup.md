---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/new-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
ms.openlocfilehash: bc9c881a69ee2365dcb9ff805c1c14fe3f1bbf79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978064"
---
# <span data-ttu-id="e0c1b-101">New-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="e0c1b-101">New-AzSqlVMGroup</span></span>

## <span data-ttu-id="e0c1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0c1b-102">SYNOPSIS</span></span>
<span data-ttu-id="e0c1b-103">새 SQL 가상 머신 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e0c1b-103">Creates a new sql virtual machine group.</span></span>

## <span data-ttu-id="e0c1b-104">구문</span><span class="sxs-lookup"><span data-stu-id="e0c1b-104">SYNTAX</span></span>

```
New-AzSqlVMGroup [-Location] <String> -Offer <String> -Sku <String> -ClusterOperatorAccount <String>
 -SqlServiceAccount <String> -StorageAccountUrl <String> -StorageAccountPrimaryKey <SecureString>
 -DomainFqdn <String> [-AsJob] [-OuPath <String>] [-FileShareWitnessPath <String>]
 [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0c1b-105">설명</span><span class="sxs-lookup"><span data-stu-id="e0c1b-105">DESCRIPTION</span></span>
<span data-ttu-id="e0c1b-106">New-AzSqlVMGroup cmdlet은 Azure SQL 가상 머신 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e0c1b-106">The New-AzSqlVMGroup cmdlet creates an Azure SQL virtual machine group.</span></span>

## <span data-ttu-id="e0c1b-107">예제</span><span class="sxs-lookup"><span data-stu-id="e0c1b-107">EXAMPLES</span></span>

### <span data-ttu-id="e0c1b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e0c1b-108">Example 1</span></span>
```powershell
PS C:\> $secureKey = ConvertTo-SecureString $profile.StorageAccountPrimaryKey -AsPlainText -Force
PS C:\> New-AzSqlVMGroup $resourceGroupName $groupName $location -ClusterOperatorAccount $profile.ClusterOperatorAccount `
>>         -SqlServiceAccount $profile.SqlServiceAccount -StorageAccountUrl $profile.StorageAccountUrl `
>>         -StorageAccountPrimaryKey $secureKey -DomainFqdn $profile.DomainFqdn `
>>         -Offer 'SQL2017-WS2016' -Sku 'Developer'
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="e0c1b-109">리소스 그룹 ResourceGroup01에서 테스트 그룹 vm을 사용하여 새 Azure SQL 가상 머신 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e0c1b-109">Creates a new Azure SQL virtual machine group with test-group vm in the resource group ResourceGroup01.</span></span>
<span data-ttu-id="e0c1b-110">$profile 형식의 개체입니다. Microsoft.Azure.Management.SqlVirtualMachine.Models.WsfcDomainProfile</span><span class="sxs-lookup"><span data-stu-id="e0c1b-110">$profile is an object of type Microsoft.Azure.Management.SqlVirtualMachine.Models.WsfcDomainProfile</span></span>

## <span data-ttu-id="e0c1b-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e0c1b-111">PARAMETERS</span></span>

### <span data-ttu-id="e0c1b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0c1b-112">-AsJob</span></span>
<span data-ttu-id="e0c1b-113">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e0c1b-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="e0c1b-114">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="e0c1b-114">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="e0c1b-115">클러스터를 만드는 데 사용되는 이름</span><span class="sxs-lookup"><span data-stu-id="e0c1b-115">Name used for creating cluster</span></span>

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

### <span data-ttu-id="e0c1b-116">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="e0c1b-116">-ClusterOperatorAccount</span></span>
<span data-ttu-id="e0c1b-117">클러스터 운영에 사용되는 이름</span><span class="sxs-lookup"><span data-stu-id="e0c1b-117">Name used for operating cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0c1b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0c1b-118">-DefaultProfile</span></span>
<span data-ttu-id="e0c1b-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e0c1b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0c1b-120">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="e0c1b-120">-DomainFqdn</span></span>
<span data-ttu-id="e0c1b-121">도메인의 완전 자격을 갖춘 이름</span><span class="sxs-lookup"><span data-stu-id="e0c1b-121">Fully qualified name of the domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0c1b-122">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="e0c1b-122">-FileShareWitnessPath</span></span>
<span data-ttu-id="e0c1b-123">파일 공유 증인에 대한 선택적 경로</span><span class="sxs-lookup"><span data-stu-id="e0c1b-123">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="e0c1b-124">-Location</span><span class="sxs-lookup"><span data-stu-id="e0c1b-124">-Location</span></span>
<span data-ttu-id="e0c1b-125">SQL 가상 머신 그룹 위치를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e0c1b-125">SQL virtual machine group location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0c1b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="e0c1b-126">-Name</span></span>
<span data-ttu-id="e0c1b-127">SQL 컴퓨터 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e0c1b-127">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0c1b-128">-제품</span><span class="sxs-lookup"><span data-stu-id="e0c1b-128">-Offer</span></span>
<span data-ttu-id="e0c1b-129">SQL 가상 머신 그룹 제품입니다.</span><span class="sxs-lookup"><span data-stu-id="e0c1b-129">SQL virtual machine group offer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0c1b-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="e0c1b-130">-OuPath</span></span>
<span data-ttu-id="e0c1b-131">노드 및 클러스터가 있는 조직 단위 경로</span><span class="sxs-lookup"><span data-stu-id="e0c1b-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="e0c1b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0c1b-132">-ResourceGroupName</span></span>
<span data-ttu-id="e0c1b-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e0c1b-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0c1b-134">-Sku</span><span class="sxs-lookup"><span data-stu-id="e0c1b-134">-Sku</span></span>
<span data-ttu-id="e0c1b-135">SQL 그룹 버전 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="e0c1b-135">SQL virtual machine group edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0c1b-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="e0c1b-136">-SqlServiceAccount</span></span>
<span data-ttu-id="e0c1b-137">클러스터의 SQL 참여하는 모든 가상 머신에서 SQL 실행되는 이름</span><span class="sxs-lookup"><span data-stu-id="e0c1b-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0c1b-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="e0c1b-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="e0c1b-139">미러링 저장소 계정의 기본 키</span><span class="sxs-lookup"><span data-stu-id="e0c1b-139">Primary key of the witness storage account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0c1b-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="e0c1b-140">-StorageAccountUrl</span></span>
<span data-ttu-id="e0c1b-141">미러링 저장소 계정의 기본 키</span><span class="sxs-lookup"><span data-stu-id="e0c1b-141">Primary key of the witness storage account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0c1b-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="e0c1b-142">-Tag</span></span>
<span data-ttu-id="e0c1b-143">가상 머신 그룹과 SQL 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="e0c1b-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="e0c1b-144">-확인</span><span class="sxs-lookup"><span data-stu-id="e0c1b-144">-Confirm</span></span>
<span data-ttu-id="e0c1b-145">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0c1b-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0c1b-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0c1b-146">-WhatIf</span></span>
<span data-ttu-id="e0c1b-147">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e0c1b-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0c1b-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e0c1b-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0c1b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0c1b-149">CommonParameters</span></span>
<span data-ttu-id="e0c1b-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e0c1b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0c1b-151">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0c1b-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0c1b-152">입력</span><span class="sxs-lookup"><span data-stu-id="e0c1b-152">INPUTS</span></span>

### <span data-ttu-id="e0c1b-153">System.String</span><span class="sxs-lookup"><span data-stu-id="e0c1b-153">System.String</span></span>

## <span data-ttu-id="e0c1b-154">출력</span><span class="sxs-lookup"><span data-stu-id="e0c1b-154">OUTPUTS</span></span>

### <span data-ttu-id="e0c1b-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="e0c1b-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="e0c1b-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e0c1b-156">NOTES</span></span>

## <span data-ttu-id="e0c1b-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0c1b-157">RELATED LINKS</span></span>
