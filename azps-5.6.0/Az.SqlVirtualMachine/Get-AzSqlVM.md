---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/get-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
ms.openlocfilehash: b3678b52f55e09fdcad8c1d116cd349b2cc5ab45
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992222"
---
# <span data-ttu-id="cdb52-101">Get-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="cdb52-101">Get-AzSqlVM</span></span>

## <span data-ttu-id="cdb52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdb52-102">SYNOPSIS</span></span>
<span data-ttu-id="cdb52-103">하나 이상의 SQL 가상 머신을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cdb52-103">Gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="cdb52-104">구문</span><span class="sxs-lookup"><span data-stu-id="cdb52-104">SYNTAX</span></span>

### <span data-ttu-id="cdb52-105">ResourceGroupOnly(기본값)</span><span class="sxs-lookup"><span data-stu-id="cdb52-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVM [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdb52-106">이름</span><span class="sxs-lookup"><span data-stu-id="cdb52-106">Name</span></span>
```
Get-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cdb52-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="cdb52-107">ResourceId</span></span>
```
Get-AzSqlVM [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdb52-108">설명</span><span class="sxs-lookup"><span data-stu-id="cdb52-108">DESCRIPTION</span></span>
<span data-ttu-id="cdb52-109">Get-AzSqlVM cmdlet은 하나 이상의 SQL 가상 머신을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cdb52-109">The Get-AzSqlVM cmdlet gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="cdb52-110">예제</span><span class="sxs-lookup"><span data-stu-id="cdb52-110">EXAMPLES</span></span>

### <span data-ttu-id="cdb52-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="cdb52-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVM

Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
vm2  ResourceGroup02    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="cdb52-112">이 명령은 현재 구독의 모든 Azure SQL 가상 머신에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cdb52-112">This command gets information about all the Azure SQL virtual machines in the current subscription.</span></span>

### <span data-ttu-id="cdb52-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="cdb52-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="cdb52-114">이 명령은 리소스 그룹 ResourceGroup01에 할당된 현재 SQL 모든 Azure SQL 가상 머신에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cdb52-114">This command gets information about all the Azure SQL virtual machines in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="cdb52-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="cdb52-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="cdb52-116">이 명령은 리소스 그룹 ResourceGroup01에 SQL 가상 머신 "vm"에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cdb52-116">This command gets information about the SQL virtual machine "vm" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="cdb52-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cdb52-117">PARAMETERS</span></span>

### <span data-ttu-id="cdb52-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdb52-118">-DefaultProfile</span></span>
<span data-ttu-id="cdb52-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cdb52-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdb52-120">-Name</span><span class="sxs-lookup"><span data-stu-id="cdb52-120">-Name</span></span>
<span data-ttu-id="cdb52-121">SQL 가상 머신 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="cdb52-121">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdb52-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdb52-122">-ResourceGroupName</span></span>
<span data-ttu-id="cdb52-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cdb52-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="cdb52-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cdb52-124">-ResourceId</span></span>
<span data-ttu-id="cdb52-125">SQL 리소스 ID를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="cdb52-125">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdb52-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdb52-126">CommonParameters</span></span>
<span data-ttu-id="cdb52-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cdb52-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdb52-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cdb52-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdb52-129">입력</span><span class="sxs-lookup"><span data-stu-id="cdb52-129">INPUTS</span></span>

### <span data-ttu-id="cdb52-130">없음</span><span class="sxs-lookup"><span data-stu-id="cdb52-130">None</span></span>

## <span data-ttu-id="cdb52-131">출력</span><span class="sxs-lookup"><span data-stu-id="cdb52-131">OUTPUTS</span></span>

### <span data-ttu-id="cdb52-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="cdb52-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="cdb52-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cdb52-133">NOTES</span></span>

## <span data-ttu-id="cdb52-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cdb52-134">RELATED LINKS</span></span>
