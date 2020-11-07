---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
ms.openlocfilehash: b23901a79262f4eb63e34b99c10b82442cb2fe6a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875605"
---
# <span data-ttu-id="b9fc6-101">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b9fc6-101">Get-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="b9fc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9fc6-102">SYNOPSIS</span></span>
<span data-ttu-id="b9fc6-103">응용 프로그램 보안 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-103">Gets an application security group.</span></span>

## <span data-ttu-id="b9fc6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b9fc6-104">SYNTAX</span></span>

```
Get-AzApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9fc6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b9fc6-105">DESCRIPTION</span></span>
<span data-ttu-id="b9fc6-106">**Get-AzApplicationSecurityGroup** cmdlet은 응용 프로그램 보안 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-106">The **Get-AzApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="b9fc6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b9fc6-107">EXAMPLES</span></span>

### <span data-ttu-id="b9fc6-108">예제 1: 모든 응용 프로그램 보안 그룹을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup
```

<span data-ttu-id="b9fc6-109">위의 명령은 구독에 있는 모든 응용 프로그램 보안 그룹을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="b9fc6-110">예제 2: 리소스 그룹의 응용 프로그램 보안 그룹을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="b9fc6-111">위의 명령은 리소스 그룹 MyResourceGroup에 속하는 모든 응용 프로그램 보안 그룹을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="b9fc6-112">예제 3: 특정 응용 프로그램 보안 그룹 검색</span><span class="sxs-lookup"><span data-stu-id="b9fc6-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup
```

<span data-ttu-id="b9fc6-113">위의 명령은 리소스 그룹 MyApplicationSecurityGroup 아래에 있는 응용 프로그램 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="b9fc6-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

## <span data-ttu-id="b9fc6-114">변수</span><span class="sxs-lookup"><span data-stu-id="b9fc6-114">PARAMETERS</span></span>

### <span data-ttu-id="b9fc6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9fc6-115">-DefaultProfile</span></span>
<span data-ttu-id="b9fc6-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9fc6-117">-이름</span><span class="sxs-lookup"><span data-stu-id="b9fc6-117">-Name</span></span>
<span data-ttu-id="b9fc6-118">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-118">The resource name.</span></span>

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

### <span data-ttu-id="b9fc6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9fc6-119">-ResourceGroupName</span></span>
<span data-ttu-id="b9fc6-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-120">The resource group name.</span></span>

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

### <span data-ttu-id="b9fc6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9fc6-121">CommonParameters</span></span>
<span data-ttu-id="b9fc6-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9fc6-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9fc6-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9fc6-124">입력</span><span class="sxs-lookup"><span data-stu-id="b9fc6-124">INPUTS</span></span>

### <span data-ttu-id="b9fc6-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b9fc6-125">System.String</span></span>

## <span data-ttu-id="b9fc6-126">출력</span><span class="sxs-lookup"><span data-stu-id="b9fc6-126">OUTPUTS</span></span>

### <span data-ttu-id="b9fc6-127">Microsoft. \* PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b9fc6-127">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="b9fc6-128">상속자</span><span class="sxs-lookup"><span data-stu-id="b9fc6-128">NOTES</span></span>

## <span data-ttu-id="b9fc6-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b9fc6-129">RELATED LINKS</span></span>

[<span data-ttu-id="b9fc6-130">새로운 AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b9fc6-130">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="b9fc6-131">제거-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b9fc6-131">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="b9fc6-132">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b9fc6-132">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b9fc6-133">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b9fc6-133">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)
