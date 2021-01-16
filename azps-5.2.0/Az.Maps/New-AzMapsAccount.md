---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/new-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
ms.openlocfilehash: 1e6358972e547e6a5fab54072396c3ad6fc7f418
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341786"
---
# <span data-ttu-id="87e83-101">New-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="87e83-101">New-AzMapsAccount</span></span>

## <span data-ttu-id="87e83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87e83-102">SYNOPSIS</span></span>
<span data-ttu-id="87e83-103">Azure Maps 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="87e83-103">Creates an Azure Maps account.</span></span>

## <span data-ttu-id="87e83-104">구문</span><span class="sxs-lookup"><span data-stu-id="87e83-104">SYNTAX</span></span>

```
New-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Tag <Hashtable[]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87e83-105">설명</span><span class="sxs-lookup"><span data-stu-id="87e83-105">DESCRIPTION</span></span>
<span data-ttu-id="87e83-106">New-AzMapsAccount cmdlet은 지정된 SKU를 사용하여 Azure Maps 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="87e83-106">The New-AzMapsAccount cmdlet creates an Azure Maps account with the specified SKU.</span></span>

## <span data-ttu-id="87e83-107">예제</span><span class="sxs-lookup"><span data-stu-id="87e83-107">EXAMPLES</span></span>

### <span data-ttu-id="87e83-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="87e83-108">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="87e83-109">SKU S0 및 태그를 사용하여 리소스 그룹 MyResourceGroup에 MyAccount라는 새 Azure Maps 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="87e83-109">Creates a new Azure Maps account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="87e83-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87e83-110">PARAMETERS</span></span>

### <span data-ttu-id="87e83-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87e83-111">-DefaultProfile</span></span>
<span data-ttu-id="87e83-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="87e83-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87e83-113">-Force</span><span class="sxs-lookup"><span data-stu-id="87e83-113">-Force</span></span>
<span data-ttu-id="87e83-114">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="87e83-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="87e83-115">-Name</span><span class="sxs-lookup"><span data-stu-id="87e83-115">-Name</span></span>
<span data-ttu-id="87e83-116">계정 이름을 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="87e83-116">Maps Account Name.</span></span>

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

### <span data-ttu-id="87e83-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87e83-117">-ResourceGroupName</span></span>
<span data-ttu-id="87e83-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87e83-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="87e83-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="87e83-119">-SkuName</span></span>
<span data-ttu-id="87e83-120">계정 SKU 이름을 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="87e83-120">Maps Account Sku Name.</span></span>

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

### <span data-ttu-id="87e83-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="87e83-121">-Tag</span></span>
<span data-ttu-id="87e83-122">계정 태그를 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="87e83-122">Maps Account Tags.</span></span>

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

### <span data-ttu-id="87e83-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87e83-123">-Confirm</span></span>
<span data-ttu-id="87e83-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="87e83-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87e83-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87e83-125">-WhatIf</span></span>
<span data-ttu-id="87e83-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="87e83-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87e83-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="87e83-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87e83-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87e83-128">CommonParameters</span></span>
<span data-ttu-id="87e83-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="87e83-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87e83-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="87e83-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87e83-131">입력</span><span class="sxs-lookup"><span data-stu-id="87e83-131">INPUTS</span></span>

### <span data-ttu-id="87e83-132">System.String</span><span class="sxs-lookup"><span data-stu-id="87e83-132">System.String</span></span>

## <span data-ttu-id="87e83-133">출력</span><span class="sxs-lookup"><span data-stu-id="87e83-133">OUTPUTS</span></span>

### <span data-ttu-id="87e83-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="87e83-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="87e83-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="87e83-135">NOTES</span></span>

## <span data-ttu-id="87e83-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="87e83-136">RELATED LINKS</span></span>
