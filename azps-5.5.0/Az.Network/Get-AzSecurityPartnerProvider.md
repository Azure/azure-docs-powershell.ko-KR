---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
ms.openlocfilehash: 8dd23c7eba3dd9306527c11afe5170740a464d2f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193737"
---
# <span data-ttu-id="983d2-101">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="983d2-101">Get-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="983d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="983d2-102">SYNOPSIS</span></span>
<span data-ttu-id="983d2-103">Azure SecurityPartnerProvider를 얻음</span><span class="sxs-lookup"><span data-stu-id="983d2-103">Get an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="983d2-104">구문</span><span class="sxs-lookup"><span data-stu-id="983d2-104">SYNTAX</span></span>

### <span data-ttu-id="983d2-105">SecurityPartnerProviderNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="983d2-105">SecurityPartnerProviderNameParameterSet (Default)</span></span>
```
Get-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="983d2-106">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="983d2-106">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Get-AzSecurityPartnerProvider -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="983d2-107">설명</span><span class="sxs-lookup"><span data-stu-id="983d2-107">DESCRIPTION</span></span>
<span data-ttu-id="983d2-108">**Get-AzSecurityPartnerProvider** cmdlet은 Azure SecurityPartnerProvider를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="983d2-108">The **Get-AzSecurityPartnerProvider** cmdlet gets an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="983d2-109">예제</span><span class="sxs-lookup"><span data-stu-id="983d2-109">EXAMPLES</span></span>

### <span data-ttu-id="983d2-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="983d2-110">Example 1</span></span>
```powershell
Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```


### <span data-ttu-id="983d2-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="983d2-111">Example 2</span></span>
```powershell
$securityPartnerProviderId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/securityPartnerProviderRG/providers/Microsoft.Network/securityPartnerProvider/securityPartnerProvider'
Get-AzSecurityPartnerProvider -ResourceId $securityPartnerProviderId
```

## <span data-ttu-id="983d2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="983d2-112">PARAMETERS</span></span>

### <span data-ttu-id="983d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="983d2-113">-DefaultProfile</span></span>
<span data-ttu-id="983d2-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="983d2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="983d2-115">-Name</span><span class="sxs-lookup"><span data-stu-id="983d2-115">-Name</span></span>
<span data-ttu-id="983d2-116">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="983d2-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="983d2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="983d2-117">-ResourceGroupName</span></span>
<span data-ttu-id="983d2-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="983d2-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="983d2-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="983d2-119">-ResourceId</span></span>
<span data-ttu-id="983d2-120">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="983d2-120">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="983d2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="983d2-121">CommonParameters</span></span>
<span data-ttu-id="983d2-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="983d2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="983d2-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="983d2-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="983d2-124">입력</span><span class="sxs-lookup"><span data-stu-id="983d2-124">INPUTS</span></span>

### <span data-ttu-id="983d2-125">System.String</span><span class="sxs-lookup"><span data-stu-id="983d2-125">System.String</span></span>

## <span data-ttu-id="983d2-126">출력</span><span class="sxs-lookup"><span data-stu-id="983d2-126">OUTPUTS</span></span>

### <span data-ttu-id="983d2-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="983d2-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="983d2-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="983d2-128">NOTES</span></span>

## <span data-ttu-id="983d2-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="983d2-129">RELATED LINKS</span></span>
