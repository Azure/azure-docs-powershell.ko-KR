---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/get-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
ms.openlocfilehash: edd98f284aa5bba6bba39c149d20a713b388bf4d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192252"
---
# <span data-ttu-id="efb2c-101">Get-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="efb2c-101">Get-AzMapsAccount</span></span>

## <span data-ttu-id="efb2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efb2c-102">SYNOPSIS</span></span>
<span data-ttu-id="efb2c-103">계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="efb2c-103">Gets the account.</span></span>

## <span data-ttu-id="efb2c-104">구문</span><span class="sxs-lookup"><span data-stu-id="efb2c-104">SYNTAX</span></span>

### <span data-ttu-id="efb2c-105">ResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="efb2c-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzMapsAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="efb2c-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="efb2c-106">AccountNameParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="efb2c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="efb2c-107">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efb2c-108">설명</span><span class="sxs-lookup"><span data-stu-id="efb2c-108">DESCRIPTION</span></span>
<span data-ttu-id="efb2c-109">Get-AzMapsAccount cmdlet은 리소스 그룹 및 이름 또는 리소스 ID로 프로비전된 Azure Maps 계정을 얻습니다. 또한 ResourceGroup의 모든 계정 목록 또는 현재 구독에 대한 모든 Azure Maps 계정 목록을 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efb2c-109">The Get-AzMapsAccount cmdlet gets a provisioned Azure Maps account, either by resource group and name, or by resource id. Additionally, it can return a list of all accounts in the ResourceGroup, or all Azure Maps accounts for the current subscription.</span></span>

## <span data-ttu-id="efb2c-110">예제</span><span class="sxs-lookup"><span data-stu-id="efb2c-110">EXAMPLES</span></span>

### <span data-ttu-id="efb2c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="efb2c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="efb2c-112">리소스 그룹 MyResourceGroup에 MyAccount라는 계정이 있는 경우 해당 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="efb2c-112">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="efb2c-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="efb2c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="efb2c-114">리소스 그룹 MyResourceGroup의 모든 Azure Maps 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="efb2c-114">Gets all Azure Maps accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="efb2c-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="efb2c-115">Example 3</span></span>
```powershell
PS C:\> Get-AzMapsAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="efb2c-116">현재 구독의 모든 Azure Maps 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="efb2c-116">Gets all Azure Maps accounts in the current subscription.</span></span>

### <span data-ttu-id="efb2c-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="efb2c-117">Example 4</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="efb2c-118">리소스 ID로 지정된 Maps 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="efb2c-118">Gets the Maps account specified by the Resource Id.</span></span>

## <span data-ttu-id="efb2c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efb2c-119">PARAMETERS</span></span>

### <span data-ttu-id="efb2c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efb2c-120">-DefaultProfile</span></span>
<span data-ttu-id="efb2c-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="efb2c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efb2c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="efb2c-122">-Name</span></span>
<span data-ttu-id="efb2c-123">계정 이름을 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="efb2c-123">Maps Account Name.</span></span>

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

### <span data-ttu-id="efb2c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efb2c-124">-ResourceGroupName</span></span>
<span data-ttu-id="efb2c-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efb2c-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="efb2c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="efb2c-126">-ResourceId</span></span>
<span data-ttu-id="efb2c-127">계정 ResourceId를 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="efb2c-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="efb2c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efb2c-128">CommonParameters</span></span>
<span data-ttu-id="efb2c-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="efb2c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efb2c-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="efb2c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efb2c-131">입력</span><span class="sxs-lookup"><span data-stu-id="efb2c-131">INPUTS</span></span>

### <span data-ttu-id="efb2c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="efb2c-132">System.String</span></span>

## <span data-ttu-id="efb2c-133">출력</span><span class="sxs-lookup"><span data-stu-id="efb2c-133">OUTPUTS</span></span>

### <span data-ttu-id="efb2c-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="efb2c-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="efb2c-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="efb2c-135">NOTES</span></span>

## <span data-ttu-id="efb2c-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="efb2c-136">RELATED LINKS</span></span>
