---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszoneconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
ms.openlocfilehash: b80889f1838945f6ba119f539c5badd59b43de61
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184409"
---
# <span data-ttu-id="69da6-101">New-AzPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="69da6-101">New-AzPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="69da6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69da6-102">SYNOPSIS</span></span>
<span data-ttu-id="69da6-103">사설 DNS 영역 그룹의 DNS 영역 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="69da6-103">Creates DNS zone configuration of the private dns zone group.</span></span>

## <span data-ttu-id="69da6-104">구문</span><span class="sxs-lookup"><span data-stu-id="69da6-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneConfig -Name <String> [-PrivateDnsZoneId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69da6-105">설명</span><span class="sxs-lookup"><span data-stu-id="69da6-105">DESCRIPTION</span></span>
<span data-ttu-id="69da6-106">**New-AzPrivateDnsZoneConfig** cmdlet을 사용하면 DNS 영역 그룹에 설정될 새 DNS 영역 구성 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="69da6-106">The **New-AzPrivateDnsZoneConfig** cmdlet enables you to create a new DNS zone configuration object which will be set on DNS zone group.</span></span>

## <span data-ttu-id="69da6-107">예제</span><span class="sxs-lookup"><span data-stu-id="69da6-107">EXAMPLES</span></span>

### <span data-ttu-id="69da6-108">DNS 영역 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="69da6-108">Creates DNS zone configuration</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
```

<span data-ttu-id="69da6-109">위의 예제에서는 DNS 영역이 만들어진 다음 DNS 영역 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="69da6-109">The above example creates DNS zone and then creates DNS zone configuration.</span></span> <span data-ttu-id="69da6-110">`New-AzPrivateDnsZone` cmdlet은 모듈 Az.PrivateDns에 의해 입증됩니다.</span><span class="sxs-lookup"><span data-stu-id="69da6-110">`New-AzPrivateDnsZone` cmdlet is proveded by module Az.PrivateDns.</span></span>

## <span data-ttu-id="69da6-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69da6-111">PARAMETERS</span></span>

### <span data-ttu-id="69da6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69da6-112">-DefaultProfile</span></span>
<span data-ttu-id="69da6-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="69da6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69da6-114">-Name</span><span class="sxs-lookup"><span data-stu-id="69da6-114">-Name</span></span>
<span data-ttu-id="69da6-115">리소스 그룹 내에서 고유한 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69da6-115">Name of the resource that is unique within a resource group.</span></span>
<span data-ttu-id="69da6-116">이 이름은 리소스에 액세스하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="69da6-116">This name can be used to access the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69da6-117">-PrivateDnsZoneId</span><span class="sxs-lookup"><span data-stu-id="69da6-117">-PrivateDnsZoneId</span></span>
<span data-ttu-id="69da6-118">사설 dns 영역의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="69da6-118">The resource id of the private dns zone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69da6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69da6-119">CommonParameters</span></span>
<span data-ttu-id="69da6-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="69da6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69da6-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="69da6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69da6-122">입력</span><span class="sxs-lookup"><span data-stu-id="69da6-122">INPUTS</span></span>

### <span data-ttu-id="69da6-123">없음</span><span class="sxs-lookup"><span data-stu-id="69da6-123">None</span></span>

## <span data-ttu-id="69da6-124">출력</span><span class="sxs-lookup"><span data-stu-id="69da6-124">OUTPUTS</span></span>

### <span data-ttu-id="69da6-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="69da6-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="69da6-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="69da6-126">NOTES</span></span>

## <span data-ttu-id="69da6-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69da6-127">RELATED LINKS</span></span>
