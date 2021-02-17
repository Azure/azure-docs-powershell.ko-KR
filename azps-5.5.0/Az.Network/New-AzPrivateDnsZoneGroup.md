---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: fff326143cf2740a085a6fcc3daa5dc89cdee646
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184404"
---
# <span data-ttu-id="7a125-101">New-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="7a125-101">New-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="7a125-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a125-102">SYNOPSIS</span></span>
<span data-ttu-id="7a125-103">지정된 개인 엔드포인트에 개인 DNS 영역 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7a125-103">Creates a private DNS zone group in the specified private endpoint.</span></span>

## <span data-ttu-id="7a125-104">구문</span><span class="sxs-lookup"><span data-stu-id="7a125-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a125-105">설명</span><span class="sxs-lookup"><span data-stu-id="7a125-105">DESCRIPTION</span></span>
<span data-ttu-id="7a125-106">**New-AzPrivateDnsZoneGroup** cmdlet을 사용하면 새 개인 DNS 영역 그룹을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a125-106">The **New-AzPrivateDnsZoneGroup** cmdlet enables you to create a new private DNS zone group.</span></span>

## <span data-ttu-id="7a125-107">예제</span><span class="sxs-lookup"><span data-stu-id="7a125-107">EXAMPLES</span></span>

### <span data-ttu-id="7a125-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7a125-108">Example 1</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
PS C:\> New-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name "dnsgroup1" -PrivateDnsZoneConfig $config -Force
Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/test-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test.vault.azure.com",
                            "RecordSets": []
                          }
                        ]
```

<span data-ttu-id="7a125-109">개인 엔드포인트가 만들어지면 위의 예제에서는 해당 개인 엔드포인트 아래에 DNS 영역 `test-pr-endpoint` 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7a125-109">Once private endpoint `test-pr-endpoint` is created, above example creates DNS zone group under that private endpoint.</span></span>

## <span data-ttu-id="7a125-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a125-110">PARAMETERS</span></span>

### <span data-ttu-id="7a125-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a125-111">-AsJob</span></span>
<span data-ttu-id="7a125-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7a125-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a125-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a125-113">-DefaultProfile</span></span>
<span data-ttu-id="7a125-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a125-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a125-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7a125-115">-Force</span></span>
<span data-ttu-id="7a125-116">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a125-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a125-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7a125-117">-Name</span></span>
<span data-ttu-id="7a125-118">사설 dns 영역 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a125-118">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a125-119">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="7a125-119">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="7a125-120">사설 dns 영역 그룹의 사설 DNS 영역 구성 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="7a125-120">A collection of private dns zone configurations of the private dns zone group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a125-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="7a125-121">-PrivateEndpointName</span></span>
<span data-ttu-id="7a125-122">개인 엔드포인트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a125-122">The name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a125-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a125-123">-ResourceGroupName</span></span>
<span data-ttu-id="7a125-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a125-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a125-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a125-125">-Confirm</span></span>
<span data-ttu-id="7a125-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a125-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a125-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a125-127">-WhatIf</span></span>
<span data-ttu-id="7a125-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7a125-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a125-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a125-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a125-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a125-130">CommonParameters</span></span>
<span data-ttu-id="7a125-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7a125-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a125-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7a125-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a125-133">입력</span><span class="sxs-lookup"><span data-stu-id="7a125-133">INPUTS</span></span>

### <span data-ttu-id="7a125-134">System.String</span><span class="sxs-lookup"><span data-stu-id="7a125-134">System.String</span></span>

### <span data-ttu-id="7a125-135">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="7a125-135">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7a125-136">출력</span><span class="sxs-lookup"><span data-stu-id="7a125-136">OUTPUTS</span></span>

### <span data-ttu-id="7a125-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="7a125-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="7a125-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7a125-138">NOTES</span></span>

## <span data-ttu-id="7a125-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a125-139">RELATED LINKS</span></span>
