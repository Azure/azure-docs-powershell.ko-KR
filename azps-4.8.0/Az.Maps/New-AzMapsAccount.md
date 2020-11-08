---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/new-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
ms.openlocfilehash: 1e6358972e547e6a5fab54072396c3ad6fc7f418
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049019"
---
# <span data-ttu-id="b416f-101">New-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="b416f-101">New-AzMapsAccount</span></span>

## <span data-ttu-id="b416f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b416f-102">SYNOPSIS</span></span>
<span data-ttu-id="b416f-103">Azure Maps 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b416f-103">Creates an Azure Maps account.</span></span>

## <span data-ttu-id="b416f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b416f-104">SYNTAX</span></span>

```
New-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Tag <Hashtable[]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b416f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b416f-105">DESCRIPTION</span></span>
<span data-ttu-id="b416f-106">New-AzMapsAccount cmdlet은 지정 된 SKU를 사용 하 여 Azure Maps 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b416f-106">The New-AzMapsAccount cmdlet creates an Azure Maps account with the specified SKU.</span></span>

## <span data-ttu-id="b416f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b416f-107">EXAMPLES</span></span>

### <span data-ttu-id="b416f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b416f-108">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="b416f-109">SKU S0 및 tag를 사용 하 여 리소스 그룹 MyResourceGroup에 내 계정 이라는 새 Azure Maps 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b416f-109">Creates a new Azure Maps account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="b416f-110">변수</span><span class="sxs-lookup"><span data-stu-id="b416f-110">PARAMETERS</span></span>

### <span data-ttu-id="b416f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b416f-111">-DefaultProfile</span></span>
<span data-ttu-id="b416f-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b416f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b416f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b416f-113">-Force</span></span>
<span data-ttu-id="b416f-114">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b416f-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="b416f-115">-이름</span><span class="sxs-lookup"><span data-stu-id="b416f-115">-Name</span></span>
<span data-ttu-id="b416f-116">계정 이름을 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="b416f-116">Maps Account Name.</span></span>

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

### <span data-ttu-id="b416f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b416f-117">-ResourceGroupName</span></span>
<span data-ttu-id="b416f-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b416f-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="b416f-119">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="b416f-119">-SkuName</span></span>
<span data-ttu-id="b416f-120">계정 Sku 이름을 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="b416f-120">Maps Account Sku Name.</span></span>

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

### <span data-ttu-id="b416f-121">태그</span><span class="sxs-lookup"><span data-stu-id="b416f-121">-Tag</span></span>
<span data-ttu-id="b416f-122">계정 태그를 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="b416f-122">Maps Account Tags.</span></span>

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

### <span data-ttu-id="b416f-123">-확인</span><span class="sxs-lookup"><span data-stu-id="b416f-123">-Confirm</span></span>
<span data-ttu-id="b416f-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b416f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b416f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b416f-125">-WhatIf</span></span>
<span data-ttu-id="b416f-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b416f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b416f-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b416f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b416f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b416f-128">CommonParameters</span></span>
<span data-ttu-id="b416f-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b416f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b416f-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b416f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b416f-131">입력</span><span class="sxs-lookup"><span data-stu-id="b416f-131">INPUTS</span></span>

### <span data-ttu-id="b416f-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b416f-132">System.String</span></span>

## <span data-ttu-id="b416f-133">출력</span><span class="sxs-lookup"><span data-stu-id="b416f-133">OUTPUTS</span></span>

### <span data-ttu-id="b416f-134">Microsoft Azure. \*. \*. \*.</span><span class="sxs-lookup"><span data-stu-id="b416f-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="b416f-135">상속자</span><span class="sxs-lookup"><span data-stu-id="b416f-135">NOTES</span></span>

## <span data-ttu-id="b416f-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b416f-136">RELATED LINKS</span></span>
