---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 5a1c519bd545ecb750f3842dac490eb31703e4d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703019"
---
# <span data-ttu-id="8cc41-101">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8cc41-101">Get-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="8cc41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cc41-102">SYNOPSIS</span></span>
<span data-ttu-id="8cc41-103">응용 프로그램 보안 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8cc41-103">Gets an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cc41-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8cc41-104">SYNTAX</span></span>

```
Get-AzureRmApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cc41-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8cc41-105">DESCRIPTION</span></span>
<span data-ttu-id="8cc41-106">**Get-AzureRmApplicationSecurityGroup** cmdlet은 응용 프로그램 보안 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8cc41-106">The **Get-AzureRmApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="8cc41-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8cc41-107">EXAMPLES</span></span>

### <span data-ttu-id="8cc41-108">예제 1: 모든 응용 프로그램 보안 그룹을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cc41-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup
```

<span data-ttu-id="8cc41-109">위의 명령은 구독에 있는 모든 응용 프로그램 보안 그룹을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cc41-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="8cc41-110">예제 2: 리소스 그룹의 응용 프로그램 보안 그룹을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cc41-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="8cc41-111">위의 명령은 리소스 그룹 MyResourceGroup에 속하는 모든 응용 프로그램 보안 그룹을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cc41-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="8cc41-112">예제 3: 특정 응용 프로그램 보안 그룹 검색</span><span class="sxs-lookup"><span data-stu-id="8cc41-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup
```

<span data-ttu-id="8cc41-113">위의 명령은 리소스 그룹 MyApplicationSecurityGroup 아래에 있는 응용 프로그램 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="8cc41-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

## <span data-ttu-id="8cc41-114">변수</span><span class="sxs-lookup"><span data-stu-id="8cc41-114">PARAMETERS</span></span>

### <span data-ttu-id="8cc41-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cc41-115">-DefaultProfile</span></span>
<span data-ttu-id="8cc41-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc41-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cc41-117">-이름</span><span class="sxs-lookup"><span data-stu-id="8cc41-117">-Name</span></span>
<span data-ttu-id="8cc41-118">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc41-118">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cc41-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cc41-119">-ResourceGroupName</span></span>
<span data-ttu-id="8cc41-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc41-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cc41-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cc41-121">CommonParameters</span></span>
<span data-ttu-id="8cc41-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cc41-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cc41-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cc41-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cc41-124">입력</span><span class="sxs-lookup"><span data-stu-id="8cc41-124">INPUTS</span></span>

### <span data-ttu-id="8cc41-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8cc41-125">System.String</span></span>

## <span data-ttu-id="8cc41-126">출력</span><span class="sxs-lookup"><span data-stu-id="8cc41-126">OUTPUTS</span></span>

### <span data-ttu-id="8cc41-127">Microsoft. \* PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8cc41-127">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="8cc41-128">상속자</span><span class="sxs-lookup"><span data-stu-id="8cc41-128">NOTES</span></span>

## <span data-ttu-id="8cc41-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8cc41-129">RELATED LINKS</span></span>

[<span data-ttu-id="8cc41-130">새로운 AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8cc41-130">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="8cc41-131">제거-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8cc41-131">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="8cc41-132">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8cc41-132">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="8cc41-133">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8cc41-133">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)
