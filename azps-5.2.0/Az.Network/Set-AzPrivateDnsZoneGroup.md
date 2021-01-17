---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: cd9270d724e0e1523c3ee621cb58fa28a2f4bc66
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364043"
---
# <span data-ttu-id="e6558-101">Set-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="e6558-101">Set-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="e6558-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6558-102">SYNOPSIS</span></span>
<span data-ttu-id="e6558-103">DNS 영역 그룹 업데이트</span><span class="sxs-lookup"><span data-stu-id="e6558-103">Updates DNS zone group</span></span>

## <span data-ttu-id="e6558-104">구문</span><span class="sxs-lookup"><span data-stu-id="e6558-104">SYNTAX</span></span>

```
Set-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6558-105">설명</span><span class="sxs-lookup"><span data-stu-id="e6558-105">DESCRIPTION</span></span>
<span data-ttu-id="e6558-106">**Set-AzPrivateDnsZoneGroup** cmdlet은 DNS 영역 그룹을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e6558-106">The **Set-AzPrivateDnsZoneGroup** cmdlet updates DNS zone group.</span></span>

## <span data-ttu-id="e6558-107">예제</span><span class="sxs-lookup"><span data-stu-id="e6558-107">EXAMPLES</span></span>

### <span data-ttu-id="e6558-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e6558-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPrivateDnsZoneGroup -ResourceGroupName rg -PrivateEndpointName my-pr-endpoint -name dnsgroup1

Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/my-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test.vault.azure.com",
                            "RecordSets": []
                          }
                        ]

PS C:\> $zone1 = Get-AzPrivateDnsZone -ResourceGroupName rg -Name "test1.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name test1-vault-azure-com -PrivateDnsZoneId $zone1.ResourceId
PS C:\> Set-AzPrivateDnsZoneGroup -ResourceGroupName rg -PrivateEndpointName my-pr-endpoint -name dnsgroup1 -PrivateDnsZoneConfig $config -Force

Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/my-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test1-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test1.vault.azure.com",
                            "RecordSets": []
                          }
                        ]
```

<span data-ttu-id="e6558-109">위의 예제에서는 dnsgroup1이라는 DNS 영역 그룹을 다른 DNS 영역으로 연결되는 새 dnsconfig로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e6558-109">Above example updates DNS zone group named dnsgroup1 with a new dnsconfig which links to another DNS zone.</span></span>

## <span data-ttu-id="e6558-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6558-110">PARAMETERS</span></span>

### <span data-ttu-id="e6558-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6558-111">-AsJob</span></span>
<span data-ttu-id="e6558-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e6558-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6558-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6558-113">-DefaultProfile</span></span>
<span data-ttu-id="e6558-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e6558-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6558-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e6558-115">-Name</span></span>
<span data-ttu-id="e6558-116">사설 dns 영역 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6558-116">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="e6558-117">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="e6558-117">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="e6558-118">사설 dns 영역 그룹의 사설 DNS 영역 구성 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="e6558-118">A collection of private dns zone configurations of the private dns zone group.</span></span>

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

### <span data-ttu-id="e6558-119">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="e6558-119">-PrivateEndpointName</span></span>
<span data-ttu-id="e6558-120">개인 엔드포인트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6558-120">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="e6558-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6558-121">-ResourceGroupName</span></span>
<span data-ttu-id="e6558-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6558-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="e6558-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6558-123">-Confirm</span></span>
<span data-ttu-id="e6558-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6558-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6558-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6558-125">-WhatIf</span></span>
<span data-ttu-id="e6558-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e6558-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6558-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6558-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6558-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6558-128">CommonParameters</span></span>
<span data-ttu-id="e6558-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e6558-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6558-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e6558-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6558-131">입력</span><span class="sxs-lookup"><span data-stu-id="e6558-131">INPUTS</span></span>

### <span data-ttu-id="e6558-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e6558-132">System.String</span></span>

### <span data-ttu-id="e6558-133">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="e6558-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e6558-134">출력</span><span class="sxs-lookup"><span data-stu-id="e6558-134">OUTPUTS</span></span>

### <span data-ttu-id="e6558-135">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="e6558-135">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="e6558-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e6558-136">NOTES</span></span>

## <span data-ttu-id="e6558-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6558-137">RELATED LINKS</span></span>
