---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
ms.openlocfilehash: b6f5b885e2cb65c8cf4775f8bb37742b8d98b6a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209149"
---
# <span data-ttu-id="a48e5-101">Get-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="a48e5-101">Get-AzSqlVM</span></span>

## <span data-ttu-id="a48e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a48e5-102">SYNOPSIS</span></span>
<span data-ttu-id="a48e5-103">하나 이상의 SQL 가상 머신을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a48e5-103">Gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="a48e5-104">구문</span><span class="sxs-lookup"><span data-stu-id="a48e5-104">SYNTAX</span></span>

### <span data-ttu-id="a48e5-105">ResourceGroupOnly(기본값)</span><span class="sxs-lookup"><span data-stu-id="a48e5-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVM [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a48e5-106">이름</span><span class="sxs-lookup"><span data-stu-id="a48e5-106">Name</span></span>
```
Get-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a48e5-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a48e5-107">ResourceId</span></span>
```
Get-AzSqlVM [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a48e5-108">설명</span><span class="sxs-lookup"><span data-stu-id="a48e5-108">DESCRIPTION</span></span>
<span data-ttu-id="a48e5-109">Get-AzSqlVM cmdlet은 하나 이상의 SQL 가상 머신을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a48e5-109">The Get-AzSqlVM cmdlet gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="a48e5-110">예제</span><span class="sxs-lookup"><span data-stu-id="a48e5-110">EXAMPLES</span></span>

### <span data-ttu-id="a48e5-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a48e5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVM

Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
vm2  ResourceGroup02    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="a48e5-112">이 명령은 현재 구독의 모든 Azure SQL 가상 머신에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a48e5-112">This command gets information about all the Azure SQL virtual machines in the current subscription.</span></span>

### <span data-ttu-id="a48e5-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="a48e5-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="a48e5-114">이 명령은 리소스 그룹 ResourceGroup01에 할당된 현재 SQL Azure 및 가상 머신에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a48e5-114">This command gets information about all the Azure SQL virtual machines in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="a48e5-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="a48e5-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="a48e5-116">이 명령은 리소스 그룹 ResourceGroup01에 SQL 가상 머신 "vm"에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a48e5-116">This command gets information about the SQL virtual machine "vm" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="a48e5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a48e5-117">PARAMETERS</span></span>

### <span data-ttu-id="a48e5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a48e5-118">-DefaultProfile</span></span>
<span data-ttu-id="a48e5-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a48e5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a48e5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a48e5-120">-Name</span></span>
<span data-ttu-id="a48e5-121">SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a48e5-121">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="a48e5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a48e5-122">-ResourceGroupName</span></span>
<span data-ttu-id="a48e5-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a48e5-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="a48e5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a48e5-124">-ResourceId</span></span>
<span data-ttu-id="a48e5-125">SQL 리소스 ID를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="a48e5-125">SQL virtual machine resource id.</span></span>

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

### <span data-ttu-id="a48e5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a48e5-126">CommonParameters</span></span>
<span data-ttu-id="a48e5-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a48e5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a48e5-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a48e5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a48e5-129">입력</span><span class="sxs-lookup"><span data-stu-id="a48e5-129">INPUTS</span></span>

### <span data-ttu-id="a48e5-130">없음</span><span class="sxs-lookup"><span data-stu-id="a48e5-130">None</span></span>

## <span data-ttu-id="a48e5-131">출력</span><span class="sxs-lookup"><span data-stu-id="a48e5-131">OUTPUTS</span></span>

### <span data-ttu-id="a48e5-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="a48e5-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="a48e5-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a48e5-133">NOTES</span></span>

## <span data-ttu-id="a48e5-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a48e5-134">RELATED LINKS</span></span>
