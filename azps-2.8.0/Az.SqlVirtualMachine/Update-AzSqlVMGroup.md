---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
ms.openlocfilehash: ea86c4e0a016ae2b33c7853ba9851762a7d8ca54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873998"
---
# <span data-ttu-id="05a1d-101">Update-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="05a1d-101">Update-AzSqlVMGroup</span></span>

## <span data-ttu-id="05a1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05a1d-102">SYNOPSIS</span></span>
<span data-ttu-id="05a1d-103">Sql 가상 컴퓨터 그룹을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="05a1d-103">Updates a sql virtual machine group.</span></span>

## <span data-ttu-id="05a1d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="05a1d-104">SYNTAX</span></span>

### <span data-ttu-id="05a1d-105">Name (기본값)</span><span class="sxs-lookup"><span data-stu-id="05a1d-105">Name (Default)</span></span>
```
Update-AzSqlVMGroup [-AsJob] [-ClusterOperatorAccount <String>] [-SqlServiceAccount <String>]
 [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>] [-DomainFqdn <String>]
 [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="05a1d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="05a1d-106">InputObject</span></span>
```
Update-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05a1d-107">리소스</span><span class="sxs-lookup"><span data-stu-id="05a1d-107">ResourceId</span></span>
```
Update-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05a1d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="05a1d-108">DESCRIPTION</span></span>
<span data-ttu-id="05a1d-109">Update-AzSqlVMGroup cmdlet은 sql 가상 컴퓨터 그룹을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="05a1d-109">The Update-AzSqlVMGroup cmdlet updates a sql virtual machine group.</span></span>

## <span data-ttu-id="05a1d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="05a1d-110">EXAMPLES</span></span>

### <span data-ttu-id="05a1d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="05a1d-111">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $group = Update-AzSqlVMGroup -InputObject $group -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="05a1d-112">Sql 가상 컴퓨터 그룹의 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="05a1d-112">Updates the tags of a sql virtual machine group.</span></span>

## <span data-ttu-id="05a1d-113">변수</span><span class="sxs-lookup"><span data-stu-id="05a1d-113">PARAMETERS</span></span>

### <span data-ttu-id="05a1d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05a1d-114">-AsJob</span></span>
<span data-ttu-id="05a1d-115">백그라운드에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="05a1d-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="05a1d-116">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="05a1d-116">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="05a1d-117">클러스터를 만드는 데 사용 된 이름</span><span class="sxs-lookup"><span data-stu-id="05a1d-117">Name used for creating cluster</span></span>

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

### <span data-ttu-id="05a1d-118">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="05a1d-118">-ClusterOperatorAccount</span></span>
<span data-ttu-id="05a1d-119">운영 클러스터에 사용 되는 이름</span><span class="sxs-lookup"><span data-stu-id="05a1d-119">Name used for operating cluster</span></span>

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

### <span data-ttu-id="05a1d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05a1d-120">-DefaultProfile</span></span>
<span data-ttu-id="05a1d-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="05a1d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05a1d-122">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="05a1d-122">-DomainFqdn</span></span>
<span data-ttu-id="05a1d-123">도메인의 정규화 된 이름</span><span class="sxs-lookup"><span data-stu-id="05a1d-123">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="05a1d-124">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="05a1d-124">-FileShareWitnessPath</span></span>
<span data-ttu-id="05a1d-125">공유 서버 감시의 선택적 경로</span><span class="sxs-lookup"><span data-stu-id="05a1d-125">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="05a1d-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05a1d-126">-InputObject</span></span>
<span data-ttu-id="05a1d-127">SQL 가상 컴퓨터 개체.</span><span class="sxs-lookup"><span data-stu-id="05a1d-127">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="05a1d-128">-이름</span><span class="sxs-lookup"><span data-stu-id="05a1d-128">-Name</span></span>
<span data-ttu-id="05a1d-129">SQL 가상 컴퓨터 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05a1d-129">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="05a1d-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="05a1d-130">-OuPath</span></span>
<span data-ttu-id="05a1d-131">노드 및 클러스터가 표시 될 조직 구성 단위 경로</span><span class="sxs-lookup"><span data-stu-id="05a1d-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="05a1d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05a1d-132">-ResourceGroupName</span></span>
<span data-ttu-id="05a1d-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05a1d-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="05a1d-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05a1d-134">-ResourceId</span></span>
<span data-ttu-id="05a1d-135">SQL 가상 컴퓨터 그룹 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="05a1d-135">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="05a1d-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="05a1d-136">-SqlServiceAccount</span></span>
<span data-ttu-id="05a1d-137">클러스터의 모든 참여 SQL 가상 컴퓨터에서 SQL 서비스를 실행할 때 사용할 수 있는 이름</span><span class="sxs-lookup"><span data-stu-id="05a1d-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="05a1d-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="05a1d-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="05a1d-139">미러링 모니터 저장소 계정의 기본 키</span><span class="sxs-lookup"><span data-stu-id="05a1d-139">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="05a1d-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="05a1d-140">-StorageAccountUrl</span></span>
<span data-ttu-id="05a1d-141">미러링 모니터 저장소 계정의 기본 키</span><span class="sxs-lookup"><span data-stu-id="05a1d-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="05a1d-142">태그</span><span class="sxs-lookup"><span data-stu-id="05a1d-142">-Tag</span></span>
<span data-ttu-id="05a1d-143">SQL 가상 컴퓨터 그룹과 연결할 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="05a1d-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="05a1d-144">-확인</span><span class="sxs-lookup"><span data-stu-id="05a1d-144">-Confirm</span></span>
<span data-ttu-id="05a1d-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="05a1d-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05a1d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05a1d-146">-WhatIf</span></span>
<span data-ttu-id="05a1d-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="05a1d-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05a1d-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="05a1d-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05a1d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05a1d-149">CommonParameters</span></span>
<span data-ttu-id="05a1d-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="05a1d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05a1d-151">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="05a1d-151">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05a1d-152">입력</span><span class="sxs-lookup"><span data-stu-id="05a1d-152">INPUTS</span></span>

### <span data-ttu-id="05a1d-153">SqlVirtualMachine를 SqlVirtualMachine 합니다. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="05a1d-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="05a1d-154">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="05a1d-154">System.String</span></span>

## <span data-ttu-id="05a1d-155">출력</span><span class="sxs-lookup"><span data-stu-id="05a1d-155">OUTPUTS</span></span>

### <span data-ttu-id="05a1d-156">SqlVirtualMachine를 SqlVirtualMachine 합니다. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="05a1d-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="05a1d-157">상속자</span><span class="sxs-lookup"><span data-stu-id="05a1d-157">NOTES</span></span>

## <span data-ttu-id="05a1d-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05a1d-158">RELATED LINKS</span></span>
