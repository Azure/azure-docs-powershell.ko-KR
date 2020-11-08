---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: fff326143cf2740a085a6fcc3daa5dc89cdee646
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218831"
---
# <span data-ttu-id="d8432-101">New-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="d8432-101">New-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="d8432-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8432-102">SYNOPSIS</span></span>
<span data-ttu-id="d8432-103">지정 된 개인 끝점에 개인 DNS 영역 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8432-103">Creates a private DNS zone group in the specified private endpoint.</span></span>

## <span data-ttu-id="d8432-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d8432-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8432-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d8432-105">DESCRIPTION</span></span>
<span data-ttu-id="d8432-106">**새로운 AzPrivateDnsZoneGroup** cmdlet을 사용 하 여 새 개인 DNS 영역 그룹을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8432-106">The **New-AzPrivateDnsZoneGroup** cmdlet enables you to create a new private DNS zone group.</span></span>

## <span data-ttu-id="d8432-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d8432-107">EXAMPLES</span></span>

### <span data-ttu-id="d8432-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d8432-108">Example 1</span></span>
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

<span data-ttu-id="d8432-109">개인 끝점 `test-pr-endpoint` 을 만든 후 위 예제에서는 해당 개인 끝점 아래에 DNS 영역 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8432-109">Once private endpoint `test-pr-endpoint` is created, above example creates DNS zone group under that private endpoint.</span></span>

## <span data-ttu-id="d8432-110">변수</span><span class="sxs-lookup"><span data-stu-id="d8432-110">PARAMETERS</span></span>

### <span data-ttu-id="d8432-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8432-111">-AsJob</span></span>
<span data-ttu-id="d8432-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d8432-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8432-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8432-113">-DefaultProfile</span></span>
<span data-ttu-id="d8432-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d8432-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8432-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d8432-115">-Force</span></span>
<span data-ttu-id="d8432-116">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="d8432-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d8432-117">-이름</span><span class="sxs-lookup"><span data-stu-id="d8432-117">-Name</span></span>
<span data-ttu-id="d8432-118">개인 dns 영역 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d8432-118">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="d8432-119">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="d8432-119">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="d8432-120">개인 dns 영역 그룹의 개인 dns 영역 구성 모음입니다.</span><span class="sxs-lookup"><span data-stu-id="d8432-120">A collection of private dns zone configurations of the private dns zone group.</span></span>

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

### <span data-ttu-id="d8432-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="d8432-121">-PrivateEndpointName</span></span>
<span data-ttu-id="d8432-122">개인 끝점의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d8432-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="d8432-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8432-123">-ResourceGroupName</span></span>
<span data-ttu-id="d8432-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d8432-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="d8432-125">-확인</span><span class="sxs-lookup"><span data-stu-id="d8432-125">-Confirm</span></span>
<span data-ttu-id="d8432-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8432-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8432-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8432-127">-WhatIf</span></span>
<span data-ttu-id="d8432-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d8432-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8432-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8432-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8432-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8432-130">CommonParameters</span></span>
<span data-ttu-id="d8432-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8432-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8432-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d8432-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8432-133">입력</span><span class="sxs-lookup"><span data-stu-id="d8432-133">INPUTS</span></span>

### <span data-ttu-id="d8432-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d8432-134">System.String</span></span>

### <span data-ttu-id="d8432-135">System.webserver. List ' 1 [[PSPrivateDnsZoneConfig, Microsoft. e. e l t. i = 2.5.0.0, Culture = 중립, PublicKeyToken = null]] 목록</span><span class="sxs-lookup"><span data-stu-id="d8432-135">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d8432-136">출력</span><span class="sxs-lookup"><span data-stu-id="d8432-136">OUTPUTS</span></span>

### <span data-ttu-id="d8432-137">PSPrivateDnsZoneGroup에 대 한.</span><span class="sxs-lookup"><span data-stu-id="d8432-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="d8432-138">상속자</span><span class="sxs-lookup"><span data-stu-id="d8432-138">NOTES</span></span>

## <span data-ttu-id="d8432-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8432-139">RELATED LINKS</span></span>
