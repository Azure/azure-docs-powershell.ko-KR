---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 32bcc3b83ad34a0f60b01048212d402745934317
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537984"
---
# <span data-ttu-id="420a4-101">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="420a4-101">Get-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="420a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="420a4-102">SYNOPSIS</span></span>
<span data-ttu-id="420a4-103">네트워크 보안 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="420a4-103">Gets a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="420a4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="420a4-104">SYNTAX</span></span>

### <span data-ttu-id="420a4-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="420a4-105">NoExpand</span></span>
```
Get-AzureRmNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="420a4-106">확장</span><span class="sxs-lookup"><span data-stu-id="420a4-106">Expand</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="420a4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="420a4-107">DESCRIPTION</span></span>
<span data-ttu-id="420a4-108">**AzureRmNetworkSecurityGroup** Cmdlet은 Azure 네트워크 보안 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="420a4-108">The **Get-AzureRmNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="420a4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="420a4-109">EXAMPLES</span></span>

### <span data-ttu-id="420a4-110">1: 기존 네트워크 보안 그룹 검색</span><span class="sxs-lookup"><span data-stu-id="420a4-110">1: Retrieve an existing network security group</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName "rg1"
```

<span data-ttu-id="420a4-111">이 명령은 리소스 그룹 "rg1"의 Azure 네트워크 보안 그룹 "nsg1"의 콘텐츠를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="420a4-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="420a4-112">변수</span><span class="sxs-lookup"><span data-stu-id="420a4-112">PARAMETERS</span></span>

### <span data-ttu-id="420a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="420a4-113">-DefaultProfile</span></span>
<span data-ttu-id="420a4-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="420a4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="420a4-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="420a4-115">-ExpandResource</span></span>
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

### <span data-ttu-id="420a4-116">-이름</span><span class="sxs-lookup"><span data-stu-id="420a4-116">-Name</span></span>
<span data-ttu-id="420a4-117">이 cmdlet이 가져오는 네트워크 보안 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="420a4-117">Specifies the name of the network security group that this cmdlet gets.</span></span>

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

### <span data-ttu-id="420a4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="420a4-118">-ResourceGroupName</span></span>
<span data-ttu-id="420a4-119">네트워크 보안 그룹이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="420a4-119">Specifies the name of the resource group that the network security group belongs to.</span></span>

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

### <span data-ttu-id="420a4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="420a4-120">CommonParameters</span></span>
<span data-ttu-id="420a4-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="420a4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="420a4-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="420a4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="420a4-123">입력</span><span class="sxs-lookup"><span data-stu-id="420a4-123">INPUTS</span></span>

### <span data-ttu-id="420a4-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="420a4-124">System.String</span></span>

## <span data-ttu-id="420a4-125">출력</span><span class="sxs-lookup"><span data-stu-id="420a4-125">OUTPUTS</span></span>

### <span data-ttu-id="420a4-126">Microsoft. 네트워크 모델. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="420a4-126">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="420a4-127">상속자</span><span class="sxs-lookup"><span data-stu-id="420a4-127">NOTES</span></span>

## <span data-ttu-id="420a4-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="420a4-128">RELATED LINKS</span></span>

[<span data-ttu-id="420a4-129">새로운 AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="420a4-129">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="420a4-130">제거-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="420a4-130">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="420a4-131">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="420a4-131">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


