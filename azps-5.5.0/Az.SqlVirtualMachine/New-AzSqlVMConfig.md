---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
ms.openlocfilehash: 0f914ab2f5c39cd53239302b2f0acd12a3e13133
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207840"
---
# <span data-ttu-id="92d67-101">New-AzSqlVMConfig</span><span class="sxs-lookup"><span data-stu-id="92d67-101">New-AzSqlVMConfig</span></span>

## <span data-ttu-id="92d67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92d67-102">SYNOPSIS</span></span>
<span data-ttu-id="92d67-103">SQL 가상 머신에 대한 새 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="92d67-103">Creates a new configuration for a sql virtual machine.</span></span>

## <span data-ttu-id="92d67-104">구문</span><span class="sxs-lookup"><span data-stu-id="92d67-104">SYNTAX</span></span>

```
New-AzSqlVMConfig [-LicenseType] <String> [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92d67-105">설명</span><span class="sxs-lookup"><span data-stu-id="92d67-105">DESCRIPTION</span></span>
<span data-ttu-id="92d67-106">New-AzSqlVMConfig cmdlet은 SQL 가상 머신에 대한 새 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="92d67-106">The New-AzSqlVMConfig cmdlet creates a new configuration object for a sql virtual machine.</span></span>

## <span data-ttu-id="92d67-107">예제</span><span class="sxs-lookup"><span data-stu-id="92d67-107">EXAMPLES</span></span>

### <span data-ttu-id="92d67-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="92d67-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzSqlVMConfig -LicenseType "PAYG"
PS C:\> New-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm" -SqlVM $config
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="92d67-109">Azure SQL 가상 머신을 만들기 위해 사용할 수 있는 SQL 가상 머신의 로컬 구성 가능한 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="92d67-109">Creates a local configurable object of sql virtual machine that can be used in order to create an Azure sql virtual machine.</span></span>

## <span data-ttu-id="92d67-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92d67-110">PARAMETERS</span></span>

### <span data-ttu-id="92d67-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92d67-111">-DefaultProfile</span></span>
<span data-ttu-id="92d67-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="92d67-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92d67-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="92d67-113">-LicenseType</span></span>
<span data-ttu-id="92d67-114">SQL 가상 머신 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="92d67-114">SQL virtual machine license type.</span></span>

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

### <span data-ttu-id="92d67-115">-Offer</span><span class="sxs-lookup"><span data-stu-id="92d67-115">-Offer</span></span>
<span data-ttu-id="92d67-116">SQL 가상 머신 제품입니다.</span><span class="sxs-lookup"><span data-stu-id="92d67-116">SQL virtual machine offer.</span></span>

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

### <span data-ttu-id="92d67-117">-Sku</span><span class="sxs-lookup"><span data-stu-id="92d67-117">-Sku</span></span>
<span data-ttu-id="92d67-118">SQL 가상 머신 버전 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="92d67-118">SQL virtual machine edition type.</span></span>

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

### <span data-ttu-id="92d67-119">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="92d67-119">-SqlManagementType</span></span>
<span data-ttu-id="92d67-120">SQL 가상 머신 관리 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="92d67-120">SQL virtual machine management type.</span></span>

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

### <span data-ttu-id="92d67-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="92d67-121">-Tag</span></span>
<span data-ttu-id="92d67-122">가상 머신과 연결하기 위한 SQL.</span><span class="sxs-lookup"><span data-stu-id="92d67-122">The tags to associate with the SQL virtual machine</span></span>

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

### <span data-ttu-id="92d67-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92d67-123">CommonParameters</span></span>
<span data-ttu-id="92d67-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="92d67-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92d67-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="92d67-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92d67-126">입력</span><span class="sxs-lookup"><span data-stu-id="92d67-126">INPUTS</span></span>

### <span data-ttu-id="92d67-127">없음</span><span class="sxs-lookup"><span data-stu-id="92d67-127">None</span></span>

## <span data-ttu-id="92d67-128">출력</span><span class="sxs-lookup"><span data-stu-id="92d67-128">OUTPUTS</span></span>

### <span data-ttu-id="92d67-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="92d67-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="92d67-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="92d67-130">NOTES</span></span>

## <span data-ttu-id="92d67-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="92d67-131">RELATED LINKS</span></span>
