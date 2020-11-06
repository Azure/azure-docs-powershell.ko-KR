---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
ms.openlocfilehash: 3a5cd755718536170c3e6fb1f6dd5410e1acffc7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537979"
---
# <span data-ttu-id="ad602-101">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ad602-101">Get-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="ad602-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad602-102">SYNOPSIS</span></span>
<span data-ttu-id="ad602-103">리소스 그룹의 가상 네트워크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ad602-103">Gets a virtual network in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad602-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ad602-104">SYNTAX</span></span>

### <span data-ttu-id="ad602-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="ad602-105">NoExpand</span></span>
```
Get-AzureRmVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad602-106">확장</span><span class="sxs-lookup"><span data-stu-id="ad602-106">Expand</span></span>
```
Get-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad602-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ad602-107">DESCRIPTION</span></span>
<span data-ttu-id="ad602-108">**AzureRmVirtualNetwork** cmdlet은 하나 이상의 가상 네트워크 n 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ad602-108">The **Get-AzureRmVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="ad602-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ad602-109">EXAMPLES</span></span>

### <span data-ttu-id="ad602-110">1: 가상 네트워크 검색</span><span class="sxs-lookup"><span data-stu-id="ad602-110">1: Retrieve a virtual network</span></span>
```
Get-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="ad602-111">이 명령은 리소스 그룹 TestResourceGroup에서 MyVirtualNetwork 이라는 가상 네트워크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ad602-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="ad602-112">변수</span><span class="sxs-lookup"><span data-stu-id="ad602-112">PARAMETERS</span></span>

### <span data-ttu-id="ad602-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad602-113">-DefaultProfile</span></span>
<span data-ttu-id="ad602-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ad602-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad602-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="ad602-115">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad602-116">-이름</span><span class="sxs-lookup"><span data-stu-id="ad602-116">-Name</span></span>
<span data-ttu-id="ad602-117">이 cmdlet이 가져오는 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad602-117">Specifies the name of the virtual network that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad602-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad602-118">-ResourceGroupName</span></span>
<span data-ttu-id="ad602-119">가상 네트워크가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad602-119">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad602-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad602-120">CommonParameters</span></span>
<span data-ttu-id="ad602-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad602-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad602-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad602-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad602-123">입력</span><span class="sxs-lookup"><span data-stu-id="ad602-123">INPUTS</span></span>

### <span data-ttu-id="ad602-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ad602-124">System.String</span></span>

## <span data-ttu-id="ad602-125">출력</span><span class="sxs-lookup"><span data-stu-id="ad602-125">OUTPUTS</span></span>

### <span data-ttu-id="ad602-126">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ad602-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="ad602-127">상속자</span><span class="sxs-lookup"><span data-stu-id="ad602-127">NOTES</span></span>

## <span data-ttu-id="ad602-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad602-128">RELATED LINKS</span></span>

[<span data-ttu-id="ad602-129">새로운 AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ad602-129">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="ad602-130">제거-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ad602-130">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="ad602-131">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ad602-131">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


