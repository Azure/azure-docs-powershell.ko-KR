---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
ms.openlocfilehash: fc4a0624b6e5702c0ef0c836f0b6ac593c25dafe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308177"
---
# <span data-ttu-id="dde5e-101">Get-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="dde5e-101">Get-AzSqlVMGroup</span></span>

## <span data-ttu-id="dde5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dde5e-102">SYNOPSIS</span></span>
<span data-ttu-id="dde5e-103">하나 이상의 sql 가상 컴퓨터 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dde5e-103">Gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="dde5e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dde5e-104">SYNTAX</span></span>

### <span data-ttu-id="dde5e-105">ResourceGroupOnly (기본값)</span><span class="sxs-lookup"><span data-stu-id="dde5e-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVMGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dde5e-106">성을</span><span class="sxs-lookup"><span data-stu-id="dde5e-106">Name</span></span>
```
Get-AzSqlVMGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dde5e-107">리소스</span><span class="sxs-lookup"><span data-stu-id="dde5e-107">ResourceId</span></span>
```
Get-AzSqlVMGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dde5e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="dde5e-108">DESCRIPTION</span></span>
<span data-ttu-id="dde5e-109">Get-AzSqlVMGroup cmdlet은 하나 이상의 sql 가상 컴퓨터 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dde5e-109">The Get-AzSqlVMGroup cmdlet gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="dde5e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="dde5e-110">EXAMPLES</span></span>

### <span data-ttu-id="dde5e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="dde5e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup

Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
group1     ResourceGroup02    Developer SQL2017-WS2016
```

<span data-ttu-id="dde5e-112">이 명령은 현재 구독의 모든 Azure SQL 가상 컴퓨터 그룹에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dde5e-112">This command gets information about all the Azure SQL virtual machine groups in the current subscription.</span></span>

### <span data-ttu-id="dde5e-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="dde5e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="dde5e-114">이 명령은 리소스 그룹 ResourceGroup01에 할당 된 현재 구독의 모든 Azure SQL 가상 컴퓨터 그룹에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dde5e-114">This command gets information about all the Azure SQL virtual machine groups in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="dde5e-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="dde5e-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="dde5e-116">이 명령은 리소스 그룹 ResourceGroup01에 할당 된 SQL 가상 컴퓨터 그룹 "test-group"에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dde5e-116">This command gets information about the SQL virtual machine group "test-group" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="dde5e-117">변수</span><span class="sxs-lookup"><span data-stu-id="dde5e-117">PARAMETERS</span></span>

### <span data-ttu-id="dde5e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dde5e-118">-DefaultProfile</span></span>
<span data-ttu-id="dde5e-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dde5e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dde5e-120">-이름</span><span class="sxs-lookup"><span data-stu-id="dde5e-120">-Name</span></span>
<span data-ttu-id="dde5e-121">SQL 가상 컴퓨터 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dde5e-121">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="dde5e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dde5e-122">-ResourceGroupName</span></span>
<span data-ttu-id="dde5e-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dde5e-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="dde5e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dde5e-124">-ResourceId</span></span>
<span data-ttu-id="dde5e-125">SQL 가상 컴퓨터 그룹 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="dde5e-125">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="dde5e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dde5e-126">CommonParameters</span></span>
<span data-ttu-id="dde5e-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde5e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dde5e-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dde5e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dde5e-129">입력</span><span class="sxs-lookup"><span data-stu-id="dde5e-129">INPUTS</span></span>

### <span data-ttu-id="dde5e-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dde5e-130">System.String</span></span>

## <span data-ttu-id="dde5e-131">출력</span><span class="sxs-lookup"><span data-stu-id="dde5e-131">OUTPUTS</span></span>

### <span data-ttu-id="dde5e-132">SqlVirtualMachine를 SqlVirtualMachine 합니다. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="dde5e-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="dde5e-133">상속자</span><span class="sxs-lookup"><span data-stu-id="dde5e-133">NOTES</span></span>

## <span data-ttu-id="dde5e-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dde5e-134">RELATED LINKS</span></span>
