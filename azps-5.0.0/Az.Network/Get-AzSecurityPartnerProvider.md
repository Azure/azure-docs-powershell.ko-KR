---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
ms.openlocfilehash: 8dd23c7eba3dd9306527c11afe5170740a464d2f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226408"
---
# <span data-ttu-id="214b4-101">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="214b4-101">Get-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="214b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="214b4-102">SYNOPSIS</span></span>
<span data-ttu-id="214b4-103">Azure SecurityPartnerProvider 다운로드</span><span class="sxs-lookup"><span data-stu-id="214b4-103">Get an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="214b4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="214b4-104">SYNTAX</span></span>

### <span data-ttu-id="214b4-105">SecurityPartnerProviderNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="214b4-105">SecurityPartnerProviderNameParameterSet (Default)</span></span>
```
Get-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="214b4-106">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="214b4-106">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Get-AzSecurityPartnerProvider -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="214b4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="214b4-107">DESCRIPTION</span></span>
<span data-ttu-id="214b4-108">**AzSecurityPartnerProvider** Cmdlet은 Azure SecurityPartnerProvider를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="214b4-108">The **Get-AzSecurityPartnerProvider** cmdlet gets an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="214b4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="214b4-109">EXAMPLES</span></span>

### <span data-ttu-id="214b4-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="214b4-110">Example 1</span></span>
```powershell
Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```


### <span data-ttu-id="214b4-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="214b4-111">Example 2</span></span>
```powershell
$securityPartnerProviderId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/securityPartnerProviderRG/providers/Microsoft.Network/securityPartnerProvider/securityPartnerProvider'
Get-AzSecurityPartnerProvider -ResourceId $securityPartnerProviderId
```

## <span data-ttu-id="214b4-112">변수</span><span class="sxs-lookup"><span data-stu-id="214b4-112">PARAMETERS</span></span>

### <span data-ttu-id="214b4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="214b4-113">-DefaultProfile</span></span>
<span data-ttu-id="214b4-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="214b4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="214b4-115">-이름</span><span class="sxs-lookup"><span data-stu-id="214b4-115">-Name</span></span>
<span data-ttu-id="214b4-116">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="214b4-116">The resource name.</span></span>

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

### <span data-ttu-id="214b4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="214b4-117">-ResourceGroupName</span></span>
<span data-ttu-id="214b4-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="214b4-118">The resource group name.</span></span>

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

### <span data-ttu-id="214b4-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="214b4-119">-ResourceId</span></span>
<span data-ttu-id="214b4-120">리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="214b4-120">The resource Id.</span></span>

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

### <span data-ttu-id="214b4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="214b4-121">CommonParameters</span></span>
<span data-ttu-id="214b4-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="214b4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="214b4-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="214b4-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="214b4-124">입력</span><span class="sxs-lookup"><span data-stu-id="214b4-124">INPUTS</span></span>

### <span data-ttu-id="214b4-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="214b4-125">System.String</span></span>

## <span data-ttu-id="214b4-126">출력</span><span class="sxs-lookup"><span data-stu-id="214b4-126">OUTPUTS</span></span>

### <span data-ttu-id="214b4-127">PSSecurityPartnerProvider에 대 한.</span><span class="sxs-lookup"><span data-stu-id="214b4-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="214b4-128">상속자</span><span class="sxs-lookup"><span data-stu-id="214b4-128">NOTES</span></span>

## <span data-ttu-id="214b4-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="214b4-129">RELATED LINKS</span></span>
