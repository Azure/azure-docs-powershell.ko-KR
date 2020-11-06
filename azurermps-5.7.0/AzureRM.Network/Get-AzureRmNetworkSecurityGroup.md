---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: dc9934aaee7706e3577039bdb77c5a6a54c29c34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532763"
---
# <span data-ttu-id="4af5b-101">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4af5b-101">Get-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="4af5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4af5b-102">SYNOPSIS</span></span>
<span data-ttu-id="4af5b-103">네트워크 보안 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4af5b-103">Gets a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4af5b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4af5b-104">SYNTAX</span></span>

### <span data-ttu-id="4af5b-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="4af5b-105">NoExpand</span></span>
```
Get-AzureRmNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4af5b-106">확장</span><span class="sxs-lookup"><span data-stu-id="4af5b-106">Expand</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4af5b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4af5b-107">DESCRIPTION</span></span>
<span data-ttu-id="4af5b-108">**AzureRmNetworkSecurityGroup** Cmdlet은 Azure 네트워크 보안 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4af5b-108">The **Get-AzureRmNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="4af5b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4af5b-109">EXAMPLES</span></span>

### <span data-ttu-id="4af5b-110">1: 기존 네트워크 보안 그룹 검색</span><span class="sxs-lookup"><span data-stu-id="4af5b-110">1: Retrieve an existing network security group</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName "rg1"
```

<span data-ttu-id="4af5b-111">이 명령은 리소스 그룹 "rg1"의 Azure 네트워크 보안 그룹 "nsg1"의 콘텐츠를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4af5b-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="4af5b-112">변수</span><span class="sxs-lookup"><span data-stu-id="4af5b-112">PARAMETERS</span></span>

### <span data-ttu-id="4af5b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4af5b-113">-DefaultProfile</span></span>
<span data-ttu-id="4af5b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4af5b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5b-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="4af5b-115">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4af5b-116">-이름</span><span class="sxs-lookup"><span data-stu-id="4af5b-116">-Name</span></span>
<span data-ttu-id="4af5b-117">이 cmdlet이 가져오는 네트워크 보안 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4af5b-117">Specifies the name of the network security group that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4af5b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4af5b-118">-ResourceGroupName</span></span>
<span data-ttu-id="4af5b-119">네트워크 보안 그룹이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4af5b-119">Specifies the name of the resource group that the network security group belongs to.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4af5b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4af5b-120">CommonParameters</span></span>
<span data-ttu-id="4af5b-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4af5b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4af5b-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4af5b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4af5b-123">입력</span><span class="sxs-lookup"><span data-stu-id="4af5b-123">INPUTS</span></span>

### <span data-ttu-id="4af5b-124">않아야</span><span class="sxs-lookup"><span data-stu-id="4af5b-124">None</span></span>
<span data-ttu-id="4af5b-125">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4af5b-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4af5b-126">출력</span><span class="sxs-lookup"><span data-stu-id="4af5b-126">OUTPUTS</span></span>

### <span data-ttu-id="4af5b-127">Microsoft. 네트워크 모델. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4af5b-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="4af5b-128">상속자</span><span class="sxs-lookup"><span data-stu-id="4af5b-128">NOTES</span></span>

## <span data-ttu-id="4af5b-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4af5b-129">RELATED LINKS</span></span>

[<span data-ttu-id="4af5b-130">새로운 AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4af5b-130">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="4af5b-131">제거-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4af5b-131">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="4af5b-132">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4af5b-132">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


