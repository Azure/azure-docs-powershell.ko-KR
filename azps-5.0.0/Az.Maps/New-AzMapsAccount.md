---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/new-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
ms.openlocfilehash: 1e6358972e547e6a5fab54072396c3ad6fc7f418
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226822"
---
# <span data-ttu-id="fa5d9-101">New-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="fa5d9-101">New-AzMapsAccount</span></span>

## <span data-ttu-id="fa5d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa5d9-102">SYNOPSIS</span></span>
<span data-ttu-id="fa5d9-103">Azure Maps 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fa5d9-103">Creates an Azure Maps account.</span></span>

## <span data-ttu-id="fa5d9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fa5d9-104">SYNTAX</span></span>

```
New-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Tag <Hashtable[]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa5d9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fa5d9-105">DESCRIPTION</span></span>
<span data-ttu-id="fa5d9-106">New-AzMapsAccount cmdlet은 지정 된 SKU를 사용 하 여 Azure Maps 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fa5d9-106">The New-AzMapsAccount cmdlet creates an Azure Maps account with the specified SKU.</span></span>

## <span data-ttu-id="fa5d9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fa5d9-107">EXAMPLES</span></span>

### <span data-ttu-id="fa5d9-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fa5d9-108">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="fa5d9-109">SKU S0 및 tag를 사용 하 여 리소스 그룹 MyResourceGroup에 내 계정 이라는 새 Azure Maps 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fa5d9-109">Creates a new Azure Maps account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="fa5d9-110">변수</span><span class="sxs-lookup"><span data-stu-id="fa5d9-110">PARAMETERS</span></span>

### <span data-ttu-id="fa5d9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa5d9-111">-DefaultProfile</span></span>
<span data-ttu-id="fa5d9-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fa5d9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa5d9-113">-Force</span><span class="sxs-lookup"><span data-stu-id="fa5d9-113">-Force</span></span>
<span data-ttu-id="fa5d9-114">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa5d9-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="fa5d9-115">-이름</span><span class="sxs-lookup"><span data-stu-id="fa5d9-115">-Name</span></span>
<span data-ttu-id="fa5d9-116">계정 이름을 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="fa5d9-116">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa5d9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa5d9-117">-ResourceGroupName</span></span>
<span data-ttu-id="fa5d9-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fa5d9-118">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa5d9-119">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="fa5d9-119">-SkuName</span></span>
<span data-ttu-id="fa5d9-120">계정 Sku 이름을 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="fa5d9-120">Maps Account Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa5d9-121">태그</span><span class="sxs-lookup"><span data-stu-id="fa5d9-121">-Tag</span></span>
<span data-ttu-id="fa5d9-122">계정 태그를 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="fa5d9-122">Maps Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa5d9-123">-확인</span><span class="sxs-lookup"><span data-stu-id="fa5d9-123">-Confirm</span></span>
<span data-ttu-id="fa5d9-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa5d9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa5d9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa5d9-125">-WhatIf</span></span>
<span data-ttu-id="fa5d9-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fa5d9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa5d9-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa5d9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa5d9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa5d9-128">CommonParameters</span></span>
<span data-ttu-id="fa5d9-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa5d9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa5d9-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa5d9-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa5d9-131">입력</span><span class="sxs-lookup"><span data-stu-id="fa5d9-131">INPUTS</span></span>

### <span data-ttu-id="fa5d9-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fa5d9-132">System.String</span></span>

## <span data-ttu-id="fa5d9-133">출력</span><span class="sxs-lookup"><span data-stu-id="fa5d9-133">OUTPUTS</span></span>

### <span data-ttu-id="fa5d9-134">Microsoft Azure. \*. \*. \*.</span><span class="sxs-lookup"><span data-stu-id="fa5d9-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="fa5d9-135">상속자</span><span class="sxs-lookup"><span data-stu-id="fa5d9-135">NOTES</span></span>

## <span data-ttu-id="fa5d9-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fa5d9-136">RELATED LINKS</span></span>
