---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
ms.openlocfilehash: f1ba6e50c03fffbd4eb6407e90e2a50957806539
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878650"
---
# <span data-ttu-id="20fca-101">Get-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="20fca-101">Get-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="20fca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20fca-102">SYNOPSIS</span></span>
<span data-ttu-id="20fca-103">SQL 가상 컴퓨터 그룹에서 하나 이상의 가용성 그룹 수신기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="20fca-103">Get one or more Availability Group Listeners in a SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="20fca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="20fca-104">SYNTAX</span></span>

### <span data-ttu-id="20fca-105">Name (기본값)</span><span class="sxs-lookup"><span data-stu-id="20fca-105">Name (Default)</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-ResourceGroupName] <String> [-SqlVMGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20fca-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="20fca-106">SqlVmGroupObject</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20fca-107">리소스</span><span class="sxs-lookup"><span data-stu-id="20fca-107">ResourceId</span></span>
```
Get-AzAvailabilityGroupListener [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="20fca-108">설명은</span><span class="sxs-lookup"><span data-stu-id="20fca-108">DESCRIPTION</span></span>
<span data-ttu-id="20fca-109">Get-AzAvailabilityGroupListener는 SQL 가상 컴퓨터 그룹에서 하나 이상의 가용성 그룹 수신기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="20fca-109">The Get-AzAvailabilityGroupListener gets one or more Availability Group Listener from the SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="20fca-110">예제의</span><span class="sxs-lookup"><span data-stu-id="20fca-110">EXAMPLES</span></span>

### <span data-ttu-id="20fca-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="20fca-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="20fca-112">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="20fca-112">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="20fca-113">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="20fca-113">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="20fca-114">이 명령은 SQL 가상 머신 그룹 SqlVmGroup01 및 리소스 그룹 ResourceGroup01에서 가용성 그룹 수신기 AgListener01에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="20fca-114">This command gets information about the Availability Group Listener AgListener01 in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="20fca-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="20fca-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
```

<span data-ttu-id="20fca-116">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="20fca-116">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="20fca-117">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="20fca-117">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="20fca-118">이 명령은 SQL 가상 머신 그룹 SqlVmGroup01 및 리소스 그룹 ResourceGroup01의 모든 가용성 그룹 수신기에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="20fca-118">This command gets information about all Availability Group Listeners in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="20fca-119">예제 3</span><span class="sxs-lookup"><span data-stu-id="20fca-119">Example 3</span></span>
```powershell
PS C:\> $SqlVmGroupObject = Get-AzSqlVMGroup -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
PS C:\> Get-AzAvailabilityGroupListener -Name AgListener01 -SqlVMGroupObject $SqlVmGroupObject
```

<span data-ttu-id="20fca-120">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="20fca-120">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="20fca-121">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="20fca-121">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

## <span data-ttu-id="20fca-122">변수</span><span class="sxs-lookup"><span data-stu-id="20fca-122">PARAMETERS</span></span>

### <span data-ttu-id="20fca-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20fca-123">-DefaultProfile</span></span>
<span data-ttu-id="20fca-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="20fca-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20fca-125">-이름</span><span class="sxs-lookup"><span data-stu-id="20fca-125">-Name</span></span>
<span data-ttu-id="20fca-126">가용성 그룹 수신기 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20fca-126">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, SqlVmGroupObject
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20fca-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20fca-127">-ResourceGroupName</span></span>
<span data-ttu-id="20fca-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20fca-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="20fca-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20fca-129">-ResourceId</span></span>
<span data-ttu-id="20fca-130">가용성 그룹 수신기 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="20fca-130">Availability Group Listener Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20fca-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="20fca-131">-SqlVMGroupName</span></span>
<span data-ttu-id="20fca-132">SQL 가상 컴퓨터 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20fca-132">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20fca-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="20fca-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="20fca-134">SQL 가상 컴퓨터 그룹 개체</span><span class="sxs-lookup"><span data-stu-id="20fca-134">SQL virtual machine Group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: SqlVmGroupObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20fca-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20fca-135">CommonParameters</span></span>
<span data-ttu-id="20fca-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="20fca-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20fca-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="20fca-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20fca-138">입력</span><span class="sxs-lookup"><span data-stu-id="20fca-138">INPUTS</span></span>

### <span data-ttu-id="20fca-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="20fca-139">System.String</span></span>

### <span data-ttu-id="20fca-140">SqlVirtualMachine를 SqlVirtualMachine 합니다. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="20fca-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="20fca-141">출력</span><span class="sxs-lookup"><span data-stu-id="20fca-141">OUTPUTS</span></span>

### <span data-ttu-id="20fca-142">SqlVirtualMachine를 SqlVirtualMachine 합니다. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="20fca-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="20fca-143">상속자</span><span class="sxs-lookup"><span data-stu-id="20fca-143">NOTES</span></span>

## <span data-ttu-id="20fca-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20fca-144">RELATED LINKS</span></span>
