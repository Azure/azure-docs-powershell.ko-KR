---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: fc1c3a9641134c113713dab0c53b22027f2b7280
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958267"
---
# <span data-ttu-id="d12de-101">New-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="d12de-101">New-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="d12de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d12de-102">SYNOPSIS</span></span>
<span data-ttu-id="d12de-103">지정된 개인 엔드포인트에 개인 DNS 영역 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d12de-103">Creates a private DNS zone group in the specified private endpoint.</span></span>

## <span data-ttu-id="d12de-104">구문</span><span class="sxs-lookup"><span data-stu-id="d12de-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d12de-105">설명</span><span class="sxs-lookup"><span data-stu-id="d12de-105">DESCRIPTION</span></span>
<span data-ttu-id="d12de-106">**New-AzPrivateDnsZoneGroup** cmdlet을 사용하면 새 개인 DNS 영역 그룹을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d12de-106">The **New-AzPrivateDnsZoneGroup** cmdlet enables you to create a new private DNS zone group.</span></span>

## <span data-ttu-id="d12de-107">예제</span><span class="sxs-lookup"><span data-stu-id="d12de-107">EXAMPLES</span></span>

### <span data-ttu-id="d12de-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d12de-108">Example 1</span></span>
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

<span data-ttu-id="d12de-109">개인 엔드포인트가 만들어지면 위의 예제에서는 해당 개인 `test-pr-endpoint` 엔드포인트 아래에 DNS 영역 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d12de-109">Once private endpoint `test-pr-endpoint` is created, above example creates DNS zone group under that private endpoint.</span></span>

## <span data-ttu-id="d12de-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d12de-110">PARAMETERS</span></span>

### <span data-ttu-id="d12de-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d12de-111">-AsJob</span></span>
<span data-ttu-id="d12de-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d12de-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d12de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d12de-113">-DefaultProfile</span></span>
<span data-ttu-id="d12de-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d12de-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d12de-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d12de-115">-Force</span></span>
<span data-ttu-id="d12de-116">리소스를 덮어 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d12de-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d12de-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d12de-117">-Name</span></span>
<span data-ttu-id="d12de-118">개인 dns 영역 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d12de-118">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="d12de-119">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="d12de-119">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="d12de-120">개인 dns 영역 그룹의 개인 dns 영역 구성의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="d12de-120">A collection of private dns zone configurations of the private dns zone group.</span></span>

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

### <span data-ttu-id="d12de-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="d12de-121">-PrivateEndpointName</span></span>
<span data-ttu-id="d12de-122">개인 엔드포인트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d12de-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="d12de-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d12de-123">-ResourceGroupName</span></span>
<span data-ttu-id="d12de-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d12de-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="d12de-125">-확인</span><span class="sxs-lookup"><span data-stu-id="d12de-125">-Confirm</span></span>
<span data-ttu-id="d12de-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d12de-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d12de-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d12de-127">-WhatIf</span></span>
<span data-ttu-id="d12de-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d12de-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d12de-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d12de-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d12de-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d12de-130">CommonParameters</span></span>
<span data-ttu-id="d12de-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d12de-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d12de-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d12de-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d12de-133">입력</span><span class="sxs-lookup"><span data-stu-id="d12de-133">INPUTS</span></span>

### <span data-ttu-id="d12de-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d12de-134">System.String</span></span>

### <span data-ttu-id="d12de-135">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="d12de-135">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d12de-136">출력</span><span class="sxs-lookup"><span data-stu-id="d12de-136">OUTPUTS</span></span>

### <span data-ttu-id="d12de-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="d12de-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="d12de-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d12de-138">NOTES</span></span>

## <span data-ttu-id="d12de-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d12de-139">RELATED LINKS</span></span>
