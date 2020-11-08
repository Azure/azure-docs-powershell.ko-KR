---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: dc90facde7d79b308ff456be9f2df1b8c087a4a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218580"
---
# <span data-ttu-id="eef09-101">Get-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="eef09-101">Get-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="eef09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eef09-102">SYNOPSIS</span></span>
<span data-ttu-id="eef09-103">개인 DNS 영역 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eef09-103">Gets private DNS zone group</span></span>

## <span data-ttu-id="eef09-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eef09-104">SYNTAX</span></span>

### <span data-ttu-id="eef09-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="eef09-105">List (Default)</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eef09-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="eef09-106">GetByName</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eef09-107">설명은</span><span class="sxs-lookup"><span data-stu-id="eef09-107">DESCRIPTION</span></span>
<span data-ttu-id="eef09-108">**AzPrivateDnsZoneGroup** cmdlet은 하나 이상의 개인 DNS 영역 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eef09-108">The **Get-AzPrivateDnsZoneGroup** cmdlet gets one or more private DNS zone groups.</span></span>

## <span data-ttu-id="eef09-109">예제의</span><span class="sxs-lookup"><span data-stu-id="eef09-109">EXAMPLES</span></span>

### <span data-ttu-id="eef09-110">예제 1: 개인 DNS 영역 그룹 검색</span><span class="sxs-lookup"><span data-stu-id="eef09-110">Example 1: Retrieve private DNS zone group</span></span>
```powershell
PS C:\> Get-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name "dnsgroup1"
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

<span data-ttu-id="eef09-111">위 예제에서는 리소스 그룹 rg의 dnsgroup1 이라는 개인 DNS 영역 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eef09-111">Above example gets a private DNS zone group named dnsgroup1 in the resource group rg.</span></span>

## <span data-ttu-id="eef09-112">변수</span><span class="sxs-lookup"><span data-stu-id="eef09-112">PARAMETERS</span></span>

### <span data-ttu-id="eef09-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eef09-113">-DefaultProfile</span></span>
<span data-ttu-id="eef09-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eef09-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eef09-115">-이름</span><span class="sxs-lookup"><span data-stu-id="eef09-115">-Name</span></span>
<span data-ttu-id="eef09-116">개인 dns 영역 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eef09-116">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eef09-117">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="eef09-117">-PrivateEndpointName</span></span>
<span data-ttu-id="eef09-118">개인 끝점의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eef09-118">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="eef09-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eef09-119">-ResourceGroupName</span></span>
<span data-ttu-id="eef09-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eef09-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="eef09-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eef09-121">CommonParameters</span></span>
<span data-ttu-id="eef09-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eef09-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eef09-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="eef09-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eef09-124">입력</span><span class="sxs-lookup"><span data-stu-id="eef09-124">INPUTS</span></span>

### <span data-ttu-id="eef09-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="eef09-125">System.String</span></span>

## <span data-ttu-id="eef09-126">출력</span><span class="sxs-lookup"><span data-stu-id="eef09-126">OUTPUTS</span></span>

### <span data-ttu-id="eef09-127">PSPrivateDnsZoneGroup에 대 한.</span><span class="sxs-lookup"><span data-stu-id="eef09-127">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="eef09-128">상속자</span><span class="sxs-lookup"><span data-stu-id="eef09-128">NOTES</span></span>

## <span data-ttu-id="eef09-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eef09-129">RELATED LINKS</span></span>
