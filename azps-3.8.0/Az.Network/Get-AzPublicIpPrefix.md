---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
ms.openlocfilehash: 35e6496cf8dbbcc9bb183bef2e8c83f7fba4a9b1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043298"
---
# <span data-ttu-id="8d935-101">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="8d935-101">Get-AzPublicIpPrefix</span></span>

## <span data-ttu-id="8d935-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d935-102">SYNOPSIS</span></span>
<span data-ttu-id="8d935-103">공용 IP 접두사를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d935-103">Gets a public IP prefix</span></span>

## <span data-ttu-id="8d935-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8d935-104">SYNTAX</span></span>

### <span data-ttu-id="8d935-105">ListParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8d935-105">ListParameterSet (Default)</span></span>
```
Get-AzPublicIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8d935-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d935-106">GetByResourceIdParameterSet</span></span>
```
Get-AzPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d935-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8d935-107">DESCRIPTION</span></span>
<span data-ttu-id="8d935-108">**AzPublicIpPrefix** cmdlet은 리소스 그룹에 하나 이상의 공용 IP 접두사를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d935-108">The **Get-AzPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="8d935-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8d935-109">EXAMPLES</span></span>

### <span data-ttu-id="8d935-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="8d935-110">Example 1</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -ResourceGroupName myRg -Name myPublicIpPrefix1

Name                   : myPublicIpPrefix1
ResourceGroupName      : myRg
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Mic
                         rosoft.Network/publicIPPrefixes/myPublicIpPrefix1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
PublicIpAddressVersion : IPv4
PrefixLength           : 28
IPPrefix               : xx.xx.xx.xx/xx
IdleTimeoutInMinutes   :
Zones                  : {}
Sku                    : {
                           "Name": "Standard"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="8d935-111">이 명령은 리소스 그룹 myRg에서 myPublicIpPrefix1를 사용 하 여 공용 IP 접두사 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d935-111">This command gets a public IP prefix resource with myPublicIpPrefix1 in resource group myRg</span></span>

### <span data-ttu-id="8d935-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="8d935-112">Example 2</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -Name myPublicIpPrefix*

Name                   : myPublicIpPrefix1
ResourceGroupName      : myRg
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Mic
                         rosoft.Network/publicIPPrefixes/myPublicIpPrefix1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
PublicIpAddressVersion : IPv4
PrefixLength           : 28
IPPrefix               : xx.xx.xx.xx/xx
IdleTimeoutInMinutes   :
Zones                  : {}
Sku                    : {
                           "Name": "Standard"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="8d935-113">이 명령은 myPublicIpPrefix로 시작 하는 모든 공용 IP 접두사 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d935-113">This command gets all public IP prefix resources that start with myPublicIpPrefix.</span></span>

## <span data-ttu-id="8d935-114">변수</span><span class="sxs-lookup"><span data-stu-id="8d935-114">PARAMETERS</span></span>

### <span data-ttu-id="8d935-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d935-115">-DefaultProfile</span></span>
<span data-ttu-id="8d935-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8d935-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d935-117">-이름</span><span class="sxs-lookup"><span data-stu-id="8d935-117">-Name</span></span>
<span data-ttu-id="8d935-118">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d935-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="8d935-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d935-119">-ResourceGroupName</span></span>
<span data-ttu-id="8d935-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d935-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="8d935-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d935-121">-ResourceId</span></span>
<span data-ttu-id="8d935-122">리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="8d935-122">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d935-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d935-123">CommonParameters</span></span>
<span data-ttu-id="8d935-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d935-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d935-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8d935-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d935-126">입력</span><span class="sxs-lookup"><span data-stu-id="8d935-126">INPUTS</span></span>

### <span data-ttu-id="8d935-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8d935-127">System.String</span></span>

## <span data-ttu-id="8d935-128">출력</span><span class="sxs-lookup"><span data-stu-id="8d935-128">OUTPUTS</span></span>

### <span data-ttu-id="8d935-129">PSPublicIpPrefix에 대 한.</span><span class="sxs-lookup"><span data-stu-id="8d935-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="8d935-130">상속자</span><span class="sxs-lookup"><span data-stu-id="8d935-130">NOTES</span></span>

## <span data-ttu-id="8d935-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d935-131">RELATED LINKS</span></span>

[<span data-ttu-id="8d935-132">새로운 AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="8d935-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="8d935-133">제거-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="8d935-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="8d935-134">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="8d935-134">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
