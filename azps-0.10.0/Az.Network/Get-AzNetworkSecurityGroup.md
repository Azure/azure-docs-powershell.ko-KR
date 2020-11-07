---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
ms.openlocfilehash: beb2b723a0b72f7ab485846f6f55fabd4e6ef9aa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875563"
---
# <span data-ttu-id="54499-101">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="54499-101">Get-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="54499-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54499-102">SYNOPSIS</span></span>
<span data-ttu-id="54499-103">네트워크 보안 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="54499-103">Gets a network security group.</span></span>

## <span data-ttu-id="54499-104">구문과</span><span class="sxs-lookup"><span data-stu-id="54499-104">SYNTAX</span></span>

### <span data-ttu-id="54499-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="54499-105">NoExpand</span></span>
```
Get-AzNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54499-106">확장</span><span class="sxs-lookup"><span data-stu-id="54499-106">Expand</span></span>
```
Get-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54499-107">설명은</span><span class="sxs-lookup"><span data-stu-id="54499-107">DESCRIPTION</span></span>
<span data-ttu-id="54499-108">**AzNetworkSecurityGroup** Cmdlet은 Azure 네트워크 보안 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="54499-108">The **Get-AzNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="54499-109">예제의</span><span class="sxs-lookup"><span data-stu-id="54499-109">EXAMPLES</span></span>

### <span data-ttu-id="54499-110">1: 기존 네트워크 보안 그룹 검색</span><span class="sxs-lookup"><span data-stu-id="54499-110">1: Retrieve an existing network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName "rg1"
```

<span data-ttu-id="54499-111">이 명령은 리소스 그룹 "rg1"의 Azure 네트워크 보안 그룹 "nsg1"의 콘텐츠를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="54499-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="54499-112">변수</span><span class="sxs-lookup"><span data-stu-id="54499-112">PARAMETERS</span></span>

### <span data-ttu-id="54499-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54499-113">-DefaultProfile</span></span>
<span data-ttu-id="54499-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="54499-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54499-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="54499-115">-ExpandResource</span></span>
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

### <span data-ttu-id="54499-116">-이름</span><span class="sxs-lookup"><span data-stu-id="54499-116">-Name</span></span>
<span data-ttu-id="54499-117">이 cmdlet이 가져오는 네트워크 보안 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54499-117">Specifies the name of the network security group that this cmdlet gets.</span></span>

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

### <span data-ttu-id="54499-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54499-118">-ResourceGroupName</span></span>
<span data-ttu-id="54499-119">네트워크 보안 그룹이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54499-119">Specifies the name of the resource group that the network security group belongs to.</span></span>

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

### <span data-ttu-id="54499-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54499-120">CommonParameters</span></span>
<span data-ttu-id="54499-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="54499-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54499-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54499-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54499-123">입력</span><span class="sxs-lookup"><span data-stu-id="54499-123">INPUTS</span></span>

## <span data-ttu-id="54499-124">출력</span><span class="sxs-lookup"><span data-stu-id="54499-124">OUTPUTS</span></span>

### <span data-ttu-id="54499-125">Microsoft. 네트워크 모델. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="54499-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="54499-126">상속자</span><span class="sxs-lookup"><span data-stu-id="54499-126">NOTES</span></span>

## <span data-ttu-id="54499-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54499-127">RELATED LINKS</span></span>

[<span data-ttu-id="54499-128">새로운 AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="54499-128">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="54499-129">제거-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="54499-129">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="54499-130">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="54499-130">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


