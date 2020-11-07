---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpPrefix.md
ms.openlocfilehash: 772f0a3bb1198bf5c8d00ad8c0dd708c37c92366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702472"
---
# <span data-ttu-id="f2751-101">Get-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f2751-101">Get-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="f2751-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2751-102">SYNOPSIS</span></span>
<span data-ttu-id="f2751-103">공용 IP 접두사를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f2751-103">Gets a public IP prefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2751-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f2751-104">SYNTAX</span></span>

### <span data-ttu-id="f2751-105">기본값</span><span class="sxs-lookup"><span data-stu-id="f2751-105">(Default)</span></span>
```
Get-AzureRmPublicIpPrefix [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2751-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2751-106">GetByNameParameterSet</span></span>
```
Get-AzureRmPublicIpPrefix [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2751-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2751-107">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2751-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f2751-108">DESCRIPTION</span></span>
<span data-ttu-id="f2751-109">**AzureRmPublicIpPrefix** cmdlet은 리소스 그룹에 하나 이상의 공용 IP 접두사를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f2751-109">The **Get-AzureRmPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="f2751-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f2751-110">EXAMPLES</span></span>

### <span data-ttu-id="f2751-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f2751-111">Example 1</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzureRmPublicIpPrefix -ResourceGroupName $rgname -Name $prefixName
```

<span data-ttu-id="f2751-112">이 명령은 리소스 그룹의 $prefixName 있는 공용 IP 접두사 리소스를 가져옵니다 $rgName</span><span class="sxs-lookup"><span data-stu-id="f2751-112">This command gets a public IP prefix resource with $prefixName in resource group $rgName</span></span>

## <span data-ttu-id="f2751-113">변수</span><span class="sxs-lookup"><span data-stu-id="f2751-113">PARAMETERS</span></span>

### <span data-ttu-id="f2751-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2751-114">-DefaultProfile</span></span>
<span data-ttu-id="f2751-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f2751-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2751-116">-이름</span><span class="sxs-lookup"><span data-stu-id="f2751-116">-Name</span></span>
<span data-ttu-id="f2751-117">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f2751-117">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2751-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2751-118">-ResourceGroupName</span></span>
<span data-ttu-id="f2751-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f2751-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2751-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2751-120">-ResourceId</span></span>
<span data-ttu-id="f2751-121">리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="f2751-121">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2751-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2751-122">CommonParameters</span></span>
<span data-ttu-id="f2751-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2751-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f2751-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2751-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2751-125">입력</span><span class="sxs-lookup"><span data-stu-id="f2751-125">INPUTS</span></span>

### <span data-ttu-id="f2751-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f2751-126">System.String</span></span>


## <span data-ttu-id="f2751-127">출력</span><span class="sxs-lookup"><span data-stu-id="f2751-127">OUTPUTS</span></span>

### <span data-ttu-id="f2751-128">PSPublicIpPrefix에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f2751-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="f2751-129">상속자</span><span class="sxs-lookup"><span data-stu-id="f2751-129">NOTES</span></span>

## <span data-ttu-id="f2751-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2751-130">RELATED LINKS</span></span>
