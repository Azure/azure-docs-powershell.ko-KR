---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azprivatednszoneconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
ms.openlocfilehash: 8ef418202025e7525dd5da74219501f11e69a5a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958315"
---
# <span data-ttu-id="23691-101">New-AzPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="23691-101">New-AzPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="23691-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23691-102">SYNOPSIS</span></span>
<span data-ttu-id="23691-103">개인 dns 영역 그룹의 DNS 영역 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="23691-103">Creates DNS zone configuration of the private dns zone group.</span></span>

## <span data-ttu-id="23691-104">구문</span><span class="sxs-lookup"><span data-stu-id="23691-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneConfig -Name <String> [-PrivateDnsZoneId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23691-105">설명</span><span class="sxs-lookup"><span data-stu-id="23691-105">DESCRIPTION</span></span>
<span data-ttu-id="23691-106">**New-AzPrivateDnsZoneConfig** cmdlet을 사용하면 DNS 영역 그룹에 설정될 새 DNS 영역 구성 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23691-106">The **New-AzPrivateDnsZoneConfig** cmdlet enables you to create a new DNS zone configuration object which will be set on DNS zone group.</span></span>

## <span data-ttu-id="23691-107">예제</span><span class="sxs-lookup"><span data-stu-id="23691-107">EXAMPLES</span></span>

### <span data-ttu-id="23691-108">DNS 영역 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="23691-108">Creates DNS zone configuration</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
```

<span data-ttu-id="23691-109">위의 예제에서는 DNS 영역을 만든 다음 DNS 영역 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="23691-109">The above example creates DNS zone and then creates DNS zone configuration.</span></span> <span data-ttu-id="23691-110">`New-AzPrivateDnsZone` cmdlet은 모듈 Az.PrivateDns로 증명됩니다.</span><span class="sxs-lookup"><span data-stu-id="23691-110">`New-AzPrivateDnsZone` cmdlet is proveded by module Az.PrivateDns.</span></span>

## <span data-ttu-id="23691-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="23691-111">PARAMETERS</span></span>

### <span data-ttu-id="23691-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23691-112">-DefaultProfile</span></span>
<span data-ttu-id="23691-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="23691-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23691-114">-Name</span><span class="sxs-lookup"><span data-stu-id="23691-114">-Name</span></span>
<span data-ttu-id="23691-115">리소스 그룹 내에서 고유한 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23691-115">Name of the resource that is unique within a resource group.</span></span>
<span data-ttu-id="23691-116">이 이름은 리소스에 액세스하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23691-116">This name can be used to access the resource.</span></span>

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

### <span data-ttu-id="23691-117">-PrivateDnsZoneId</span><span class="sxs-lookup"><span data-stu-id="23691-117">-PrivateDnsZoneId</span></span>
<span data-ttu-id="23691-118">개인 dns 영역의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="23691-118">The resource id of the private dns zone.</span></span>

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

### <span data-ttu-id="23691-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23691-119">CommonParameters</span></span>
<span data-ttu-id="23691-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="23691-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23691-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23691-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23691-122">입력</span><span class="sxs-lookup"><span data-stu-id="23691-122">INPUTS</span></span>

### <span data-ttu-id="23691-123">없음</span><span class="sxs-lookup"><span data-stu-id="23691-123">None</span></span>

## <span data-ttu-id="23691-124">출력</span><span class="sxs-lookup"><span data-stu-id="23691-124">OUTPUTS</span></span>

### <span data-ttu-id="23691-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="23691-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="23691-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="23691-126">NOTES</span></span>

## <span data-ttu-id="23691-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23691-127">RELATED LINKS</span></span>
