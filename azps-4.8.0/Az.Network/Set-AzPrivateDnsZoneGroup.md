---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: cd9270d724e0e1523c3ee621cb58fa28a2f4bc66
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94203885"
---
# <span data-ttu-id="a3774-101">Set-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="a3774-101">Set-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="a3774-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3774-102">SYNOPSIS</span></span>
<span data-ttu-id="a3774-103">DNS 영역 그룹 업데이트</span><span class="sxs-lookup"><span data-stu-id="a3774-103">Updates DNS zone group</span></span>

## <span data-ttu-id="a3774-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a3774-104">SYNTAX</span></span>

```
Set-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3774-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a3774-105">DESCRIPTION</span></span>
<span data-ttu-id="a3774-106">**Set-AzPrivateDnsZoneGroup** CMDLET 업데이트 DNS 영역 그룹</span><span class="sxs-lookup"><span data-stu-id="a3774-106">The **Set-AzPrivateDnsZoneGroup** cmdlet updates DNS zone group.</span></span>

## <span data-ttu-id="a3774-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a3774-107">EXAMPLES</span></span>

### <span data-ttu-id="a3774-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a3774-108">Example 1</span></span>
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

<span data-ttu-id="a3774-109">위 예제에서는 다른 DNS 영역에 연결 되는 new dnsconfig로 dnsgroup1 이라는 DNS 영역 그룹을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3774-109">Above example updates DNS zone group named dnsgroup1 with a new dnsconfig which links to another DNS zone.</span></span>

## <span data-ttu-id="a3774-110">변수</span><span class="sxs-lookup"><span data-stu-id="a3774-110">PARAMETERS</span></span>

### <span data-ttu-id="a3774-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3774-111">-AsJob</span></span>
<span data-ttu-id="a3774-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a3774-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3774-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3774-113">-DefaultProfile</span></span>
<span data-ttu-id="a3774-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a3774-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3774-115">-이름</span><span class="sxs-lookup"><span data-stu-id="a3774-115">-Name</span></span>
<span data-ttu-id="a3774-116">개인 dns 영역 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3774-116">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="a3774-117">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="a3774-117">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="a3774-118">개인 dns 영역 그룹의 개인 dns 영역 구성 모음입니다.</span><span class="sxs-lookup"><span data-stu-id="a3774-118">A collection of private dns zone configurations of the private dns zone group.</span></span>

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

### <span data-ttu-id="a3774-119">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="a3774-119">-PrivateEndpointName</span></span>
<span data-ttu-id="a3774-120">개인 끝점의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3774-120">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="a3774-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3774-121">-ResourceGroupName</span></span>
<span data-ttu-id="a3774-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3774-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="a3774-123">-확인</span><span class="sxs-lookup"><span data-stu-id="a3774-123">-Confirm</span></span>
<span data-ttu-id="a3774-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3774-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3774-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3774-125">-WhatIf</span></span>
<span data-ttu-id="a3774-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a3774-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3774-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a3774-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3774-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3774-128">CommonParameters</span></span>
<span data-ttu-id="a3774-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3774-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3774-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a3774-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3774-131">입력</span><span class="sxs-lookup"><span data-stu-id="a3774-131">INPUTS</span></span>

### <span data-ttu-id="a3774-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a3774-132">System.String</span></span>

### <span data-ttu-id="a3774-133">System.webserver. List ' 1 [[PSPrivateDnsZoneConfig, Microsoft. e. e l t. i = 2.5.0.0, Culture = 중립, PublicKeyToken = null]] 목록</span><span class="sxs-lookup"><span data-stu-id="a3774-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a3774-134">출력</span><span class="sxs-lookup"><span data-stu-id="a3774-134">OUTPUTS</span></span>

### <span data-ttu-id="a3774-135">PSPrivateDnsZoneGroup에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a3774-135">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="a3774-136">상속자</span><span class="sxs-lookup"><span data-stu-id="a3774-136">NOTES</span></span>

## <span data-ttu-id="a3774-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3774-137">RELATED LINKS</span></span>
