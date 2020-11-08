---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
ms.openlocfilehash: 885be17315e0dc0be8223f0d28bc11a6d6e41146
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213840"
---
# <span data-ttu-id="7f4c1-101">Update-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="7f4c1-101">Update-AzSqlVMGroup</span></span>

## <span data-ttu-id="7f4c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f4c1-102">SYNOPSIS</span></span>
<span data-ttu-id="7f4c1-103">Sql 가상 컴퓨터 그룹을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f4c1-103">Updates a sql virtual machine group.</span></span>

## <span data-ttu-id="7f4c1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7f4c1-104">SYNTAX</span></span>

### <span data-ttu-id="7f4c1-105">Name (기본값)</span><span class="sxs-lookup"><span data-stu-id="7f4c1-105">Name (Default)</span></span>
```
Update-AzSqlVMGroup [-AsJob] [-ClusterOperatorAccount <String>] [-SqlServiceAccount <String>]
 [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>] [-DomainFqdn <String>]
 [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f4c1-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7f4c1-106">InputObject</span></span>
```
Update-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f4c1-107">리소스</span><span class="sxs-lookup"><span data-stu-id="7f4c1-107">ResourceId</span></span>
```
Update-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f4c1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7f4c1-108">DESCRIPTION</span></span>
<span data-ttu-id="7f4c1-109">Update-AzSqlVMGroup cmdlet은 sql 가상 컴퓨터 그룹을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f4c1-109">The Update-AzSqlVMGroup cmdlet updates a sql virtual machine group.</span></span>

## <span data-ttu-id="7f4c1-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7f4c1-110">EXAMPLES</span></span>

### <span data-ttu-id="7f4c1-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7f4c1-111">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $group = Update-AzSqlVMGroup -InputObject $group -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="7f4c1-112">Sql 가상 컴퓨터 그룹의 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f4c1-112">Updates the tags of a sql virtual machine group.</span></span>

## <span data-ttu-id="7f4c1-113">변수</span><span class="sxs-lookup"><span data-stu-id="7f4c1-113">PARAMETERS</span></span>

### <span data-ttu-id="7f4c1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f4c1-114">-AsJob</span></span>
<span data-ttu-id="7f4c1-115">백그라운드에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f4c1-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="7f4c1-116">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="7f4c1-116">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="7f4c1-117">클러스터를 만드는 데 사용 된 이름</span><span class="sxs-lookup"><span data-stu-id="7f4c1-117">Name used for creating cluster</span></span>

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

### <span data-ttu-id="7f4c1-118">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="7f4c1-118">-ClusterOperatorAccount</span></span>
<span data-ttu-id="7f4c1-119">운영 클러스터에 사용 되는 이름</span><span class="sxs-lookup"><span data-stu-id="7f4c1-119">Name used for operating cluster</span></span>

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

### <span data-ttu-id="7f4c1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f4c1-120">-DefaultProfile</span></span>
<span data-ttu-id="7f4c1-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7f4c1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f4c1-122">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="7f4c1-122">-DomainFqdn</span></span>
<span data-ttu-id="7f4c1-123">도메인의 정규화 된 이름</span><span class="sxs-lookup"><span data-stu-id="7f4c1-123">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="7f4c1-124">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="7f4c1-124">-FileShareWitnessPath</span></span>
<span data-ttu-id="7f4c1-125">공유 서버 감시의 선택적 경로</span><span class="sxs-lookup"><span data-stu-id="7f4c1-125">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="7f4c1-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f4c1-126">-InputObject</span></span>
<span data-ttu-id="7f4c1-127">SQL 가상 컴퓨터 개체.</span><span class="sxs-lookup"><span data-stu-id="7f4c1-127">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="7f4c1-128">-이름</span><span class="sxs-lookup"><span data-stu-id="7f4c1-128">-Name</span></span>
<span data-ttu-id="7f4c1-129">SQL 가상 컴퓨터 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f4c1-129">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="7f4c1-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="7f4c1-130">-OuPath</span></span>
<span data-ttu-id="7f4c1-131">노드 및 클러스터가 표시 될 조직 구성 단위 경로</span><span class="sxs-lookup"><span data-stu-id="7f4c1-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="7f4c1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f4c1-132">-ResourceGroupName</span></span>
<span data-ttu-id="7f4c1-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f4c1-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="7f4c1-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f4c1-134">-ResourceId</span></span>
<span data-ttu-id="7f4c1-135">SQL 가상 컴퓨터 그룹 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="7f4c1-135">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="7f4c1-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="7f4c1-136">-SqlServiceAccount</span></span>
<span data-ttu-id="7f4c1-137">클러스터의 모든 참여 SQL 가상 컴퓨터에서 SQL 서비스를 실행할 때 사용할 수 있는 이름</span><span class="sxs-lookup"><span data-stu-id="7f4c1-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="7f4c1-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="7f4c1-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="7f4c1-139">미러링 모니터 저장소 계정의 기본 키</span><span class="sxs-lookup"><span data-stu-id="7f4c1-139">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="7f4c1-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="7f4c1-140">-StorageAccountUrl</span></span>
<span data-ttu-id="7f4c1-141">미러링 모니터 저장소 계정의 기본 키</span><span class="sxs-lookup"><span data-stu-id="7f4c1-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="7f4c1-142">태그</span><span class="sxs-lookup"><span data-stu-id="7f4c1-142">-Tag</span></span>
<span data-ttu-id="7f4c1-143">SQL 가상 컴퓨터 그룹과 연결할 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="7f4c1-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="7f4c1-144">-확인</span><span class="sxs-lookup"><span data-stu-id="7f4c1-144">-Confirm</span></span>
<span data-ttu-id="7f4c1-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f4c1-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f4c1-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f4c1-146">-WhatIf</span></span>
<span data-ttu-id="7f4c1-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7f4c1-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f4c1-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7f4c1-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f4c1-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f4c1-149">CommonParameters</span></span>
<span data-ttu-id="7f4c1-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f4c1-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f4c1-151">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7f4c1-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f4c1-152">입력</span><span class="sxs-lookup"><span data-stu-id="7f4c1-152">INPUTS</span></span>

### <span data-ttu-id="7f4c1-153">SqlVirtualMachine를 SqlVirtualMachine 합니다. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="7f4c1-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="7f4c1-154">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7f4c1-154">System.String</span></span>

## <span data-ttu-id="7f4c1-155">출력</span><span class="sxs-lookup"><span data-stu-id="7f4c1-155">OUTPUTS</span></span>

### <span data-ttu-id="7f4c1-156">SqlVirtualMachine를 SqlVirtualMachine 합니다. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="7f4c1-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="7f4c1-157">상속자</span><span class="sxs-lookup"><span data-stu-id="7f4c1-157">NOTES</span></span>

## <span data-ttu-id="7f4c1-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f4c1-158">RELATED LINKS</span></span>
