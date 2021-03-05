---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/get-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
ms.openlocfilehash: a7ff8df963f7d1d58256ab40cf5788e81b49a23c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992194"
---
# <span data-ttu-id="5c9a2-101">Get-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="5c9a2-101">Get-AzSqlVMGroup</span></span>

## <span data-ttu-id="5c9a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c9a2-102">SYNOPSIS</span></span>
<span data-ttu-id="5c9a2-103">하나 이상의 SQL 가상 머신 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5c9a2-103">Gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="5c9a2-104">구문</span><span class="sxs-lookup"><span data-stu-id="5c9a2-104">SYNTAX</span></span>

### <span data-ttu-id="5c9a2-105">ResourceGroupOnly(기본값)</span><span class="sxs-lookup"><span data-stu-id="5c9a2-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVMGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5c9a2-106">이름</span><span class="sxs-lookup"><span data-stu-id="5c9a2-106">Name</span></span>
```
Get-AzSqlVMGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5c9a2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c9a2-107">ResourceId</span></span>
```
Get-AzSqlVMGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c9a2-108">설명</span><span class="sxs-lookup"><span data-stu-id="5c9a2-108">DESCRIPTION</span></span>
<span data-ttu-id="5c9a2-109">Get-AzSqlVMGroup cmdlet은 하나 이상의 SQL 가상 머신 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5c9a2-109">The Get-AzSqlVMGroup cmdlet gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="5c9a2-110">예제</span><span class="sxs-lookup"><span data-stu-id="5c9a2-110">EXAMPLES</span></span>

### <span data-ttu-id="5c9a2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="5c9a2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup

Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
group1     ResourceGroup02    Developer SQL2017-WS2016
```

<span data-ttu-id="5c9a2-112">이 명령은 현재 구독의 모든 Azure SQL 가상 머신 그룹에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5c9a2-112">This command gets information about all the Azure SQL virtual machine groups in the current subscription.</span></span>

### <span data-ttu-id="5c9a2-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="5c9a2-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="5c9a2-114">이 명령은 리소스 그룹 ResourceGroup01에 할당된 현재 SQL 모든 Azure SQL 가상 머신 그룹에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5c9a2-114">This command gets information about all the Azure SQL virtual machine groups in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="5c9a2-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="5c9a2-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="5c9a2-116">이 명령은 리소스 그룹 ResourceGroup01에 SQL 가상 머신 그룹 "테스트 그룹"에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5c9a2-116">This command gets information about the SQL virtual machine group "test-group" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="5c9a2-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5c9a2-117">PARAMETERS</span></span>

### <span data-ttu-id="5c9a2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c9a2-118">-DefaultProfile</span></span>
<span data-ttu-id="5c9a2-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5c9a2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c9a2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5c9a2-120">-Name</span></span>
<span data-ttu-id="5c9a2-121">SQL 컴퓨터 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c9a2-121">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="5c9a2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c9a2-122">-ResourceGroupName</span></span>
<span data-ttu-id="5c9a2-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c9a2-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupOnly
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="5c9a2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c9a2-124">-ResourceId</span></span>
<span data-ttu-id="5c9a2-125">SQL 그룹 리소스 ID를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="5c9a2-125">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="5c9a2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c9a2-126">CommonParameters</span></span>
<span data-ttu-id="5c9a2-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5c9a2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c9a2-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c9a2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c9a2-129">입력</span><span class="sxs-lookup"><span data-stu-id="5c9a2-129">INPUTS</span></span>

### <span data-ttu-id="5c9a2-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5c9a2-130">System.String</span></span>

## <span data-ttu-id="5c9a2-131">출력</span><span class="sxs-lookup"><span data-stu-id="5c9a2-131">OUTPUTS</span></span>

### <span data-ttu-id="5c9a2-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="5c9a2-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="5c9a2-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5c9a2-133">NOTES</span></span>

## <span data-ttu-id="5c9a2-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c9a2-134">RELATED LINKS</span></span>
