---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/get-azurermmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccount.md
ms.openlocfilehash: 68ccff91f6e233862ba1ee5aa94a3a3d0d8422b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535815"
---
# <span data-ttu-id="d398c-101">Get-AzureRmMapsAccount</span><span class="sxs-lookup"><span data-stu-id="d398c-101">Get-AzureRmMapsAccount</span></span>

## <span data-ttu-id="d398c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d398c-102">SYNOPSIS</span></span>
<span data-ttu-id="d398c-103">계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d398c-103">Gets the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d398c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d398c-104">SYNTAX</span></span>

### <span data-ttu-id="d398c-105">ResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d398c-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmMapsAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d398c-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d398c-106">AccountNameParameterSet</span></span>
```
Get-AzureRmMapsAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d398c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d398c-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmMapsAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d398c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d398c-108">DESCRIPTION</span></span>
<span data-ttu-id="d398c-109">Get-AzureRmMapsAccount cmdlet은 리소스 그룹과 이름 또는 리소스 id를 기준으로 프로 비전 된 Azure Maps 계정을 가져옵니다. 또한이는 ResourceGroup의 모든 계정이 나 현재 구독에 대 한 모든 Azure Maps 계정 목록을 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d398c-109">The Get-AzureRmMapsAccount cmdlet gets a provisioned Azure Maps account, either by resource group and name, or by resource id. Additionally, it can return a list of all accounts in the ResourceGroup, or all Azure Maps accounts for the current subscription.</span></span>

## <span data-ttu-id="d398c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d398c-110">EXAMPLES</span></span>

### <span data-ttu-id="d398c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d398c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="d398c-112">리소스 그룹 MyResourceGroup에 내 계정 이라는 계정이 있는 경우 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d398c-112">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="d398c-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="d398c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="d398c-114">리소스 그룹 MyResourceGroup의 모든 Azure Maps 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d398c-114">Gets all Azure Maps accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="d398c-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="d398c-115">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="d398c-116">현재 구독의 모든 Azure Maps 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d398c-116">Gets all Azure Maps accounts in the current subscription.</span></span>

### <span data-ttu-id="d398c-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="d398c-117">Example 4</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="d398c-118">리소스 Id로 지정 된 지도 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d398c-118">Gets the Maps account specified by the Resource Id.</span></span>

## <span data-ttu-id="d398c-119">변수</span><span class="sxs-lookup"><span data-stu-id="d398c-119">PARAMETERS</span></span>

### <span data-ttu-id="d398c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d398c-120">-DefaultProfile</span></span>
<span data-ttu-id="d398c-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d398c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d398c-122">-이름</span><span class="sxs-lookup"><span data-stu-id="d398c-122">-Name</span></span>
<span data-ttu-id="d398c-123">계정 이름을 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="d398c-123">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d398c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d398c-124">-ResourceGroupName</span></span>
<span data-ttu-id="d398c-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d398c-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d398c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d398c-126">-ResourceId</span></span>
<span data-ttu-id="d398c-127">Maps 계정 ResourceId.</span><span class="sxs-lookup"><span data-stu-id="d398c-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d398c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d398c-128">CommonParameters</span></span>
<span data-ttu-id="d398c-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d398c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d398c-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d398c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d398c-131">입력</span><span class="sxs-lookup"><span data-stu-id="d398c-131">INPUTS</span></span>

### <span data-ttu-id="d398c-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d398c-132">System.String</span></span>

## <span data-ttu-id="d398c-133">출력</span><span class="sxs-lookup"><span data-stu-id="d398c-133">OUTPUTS</span></span>

### <span data-ttu-id="d398c-134">Microsoft Azure. \*. \*. \*.</span><span class="sxs-lookup"><span data-stu-id="d398c-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="d398c-135">상속자</span><span class="sxs-lookup"><span data-stu-id="d398c-135">NOTES</span></span>

## <span data-ttu-id="d398c-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d398c-136">RELATED LINKS</span></span>
