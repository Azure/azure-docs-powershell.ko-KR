---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkProfile.md
ms.openlocfilehash: 5bdd5e5d5212564afb1f9b06f220e8c452bcbbaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537988"
---
# <span data-ttu-id="dbaf6-101">Get-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dbaf6-101">Get-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="dbaf6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbaf6-102">SYNOPSIS</span></span>
<span data-ttu-id="dbaf6-103">기존 네트워크 프로필 최상위 수준 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dbaf6-103">Gets an existing network profile top level resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbaf6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dbaf6-104">SYNTAX</span></span>

### <span data-ttu-id="dbaf6-105">NoExpand (기본값)</span><span class="sxs-lookup"><span data-stu-id="dbaf6-105">NoExpand (Default)</span></span>
```
Get-AzureRmNetworkProfile [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbaf6-106">GetByResourceNameExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbaf6-106">GetByResourceNameExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbaf6-107">GetByResourceNameNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbaf6-107">GetByResourceNameNoExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile [-ResourceGroupName <String>] [-Name <String>] -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbaf6-108">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbaf6-108">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceId <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbaf6-109">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbaf6-109">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceId <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbaf6-110">설명은</span><span class="sxs-lookup"><span data-stu-id="dbaf6-110">DESCRIPTION</span></span>
<span data-ttu-id="dbaf6-111">**AzureRmNetworkProfile** cmdlet은 기존 네트워크 프로필의 상위 수준 리소스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbaf6-111">The **Get-AzureRmNetworkProfile** cmdlet retrieves an existing network profile top level resource</span></span>

## <span data-ttu-id="dbaf6-112">예제의</span><span class="sxs-lookup"><span data-stu-id="dbaf6-112">EXAMPLES</span></span>

### <span data-ttu-id="dbaf6-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="dbaf6-113">Example 1</span></span>
```powershell
$networkProfile = Get-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="dbaf6-114">이렇게 하면 리소스 그룹 rg1에서 네트워크 프로필 np1 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dbaf6-114">This retrieves the network profile np1 in resource group rg1</span></span>

## <span data-ttu-id="dbaf6-115">변수</span><span class="sxs-lookup"><span data-stu-id="dbaf6-115">PARAMETERS</span></span>

### <span data-ttu-id="dbaf6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbaf6-116">-DefaultProfile</span></span>
<span data-ttu-id="dbaf6-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dbaf6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbaf6-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="dbaf6-118">-ExpandResource</span></span>
<span data-ttu-id="dbaf6-119">확장할 리소스 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="dbaf6-119">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet, GetByResourceNameNoExpandParameterSet, GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbaf6-120">-이름</span><span class="sxs-lookup"><span data-stu-id="dbaf6-120">-Name</span></span>
<span data-ttu-id="dbaf6-121">네트워크 프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dbaf6-121">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbaf6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbaf6-122">-ResourceGroupName</span></span>
<span data-ttu-id="dbaf6-123">네트워크 프로필의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dbaf6-123">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbaf6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dbaf6-124">-ResourceId</span></span>
<span data-ttu-id="dbaf6-125">네트워크 프로필의 Azure resource manager id입니다.</span><span class="sxs-lookup"><span data-stu-id="dbaf6-125">The Azure resource manager id of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbaf6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbaf6-126">CommonParameters</span></span>
<span data-ttu-id="dbaf6-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbaf6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbaf6-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbaf6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbaf6-129">입력</span><span class="sxs-lookup"><span data-stu-id="dbaf6-129">INPUTS</span></span>

### <span data-ttu-id="dbaf6-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dbaf6-130">System.String</span></span>

## <span data-ttu-id="dbaf6-131">출력</span><span class="sxs-lookup"><span data-stu-id="dbaf6-131">OUTPUTS</span></span>

### <span data-ttu-id="dbaf6-132">Microsoft. 네트워크 모델. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dbaf6-132">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="dbaf6-133">상속자</span><span class="sxs-lookup"><span data-stu-id="dbaf6-133">NOTES</span></span>

## <span data-ttu-id="dbaf6-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dbaf6-134">RELATED LINKS</span></span>
