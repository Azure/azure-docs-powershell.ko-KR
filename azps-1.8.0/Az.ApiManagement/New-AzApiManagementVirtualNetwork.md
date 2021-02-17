---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: 496e65438a2c0ef5f09bbf961535eaa842062f25
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400895"
---
# <span data-ttu-id="cecc4-101">New-AzApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cecc4-101">New-AzApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="cecc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cecc4-102">SYNOPSIS</span></span>
<span data-ttu-id="cecc4-103">PsApiManagementVirtualNetwork의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cecc4-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

## <span data-ttu-id="cecc4-104">구문</span><span class="sxs-lookup"><span data-stu-id="cecc4-104">SYNTAX</span></span>

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cecc4-105">설명</span><span class="sxs-lookup"><span data-stu-id="cecc4-105">DESCRIPTION</span></span>
<span data-ttu-id="cecc4-106">**New-AzApiManagementVirtualNetwork** cmdlet은 **PsApiManagementVirtualNetwork의** 인스턴스를 만드는 도우미 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="cecc4-106">The **New-AzApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="cecc4-107">이 명령은 **Set-AzApiManagement** cmdlet과 함께 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="cecc4-107">This command is used with **Set-AzApiManagement** cmdlet.</span></span>

## <span data-ttu-id="cecc4-108">예제</span><span class="sxs-lookup"><span data-stu-id="cecc4-108">EXAMPLES</span></span>

### <span data-ttu-id="cecc4-109">예제 1: 가상 네트워크 만들기</span><span class="sxs-lookup"><span data-stu-id="cecc4-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$vnetName = "myvnet"
PS C:\>$subnetName = "default"
PS C:\>$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.1.0/24
PS C:\>$vnet = New-AzvirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix 10.0.0.0/16 -Subnet $subnet

# Create a Virtual Network Object
PS C:\>$virtualNetwork = New-AzApiManagementVirtualNetwork -Location $location -SubnetResourceId $vnet.Subnets[0].Id

# Get the service
PS C:\>$service = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$service.VirtualNetwork = $virtualNetwork
PS C:\>$service.VpnType = "External"

# Update the Deployment with Virtual Network
PS C:\>Set-AzApiManagement -ApiManagement $service
```

<span data-ttu-id="cecc4-110">이 예제에서는 가상 네트워크를 만든 다음 **Set-AzApiManagement** cmdlet을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="cecc4-110">This example creates a virtual network and then calls the **Set-AzApiManagement** cmdlet.</span></span>

## <span data-ttu-id="cecc4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cecc4-111">PARAMETERS</span></span>

### <span data-ttu-id="cecc4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cecc4-112">-DefaultProfile</span></span>
<span data-ttu-id="cecc4-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cecc4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cecc4-114">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="cecc4-114">-SubnetResourceId</span></span>
<span data-ttu-id="cecc4-115">가상 네트워크의 서브넷 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cecc4-115">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="cecc4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cecc4-116">CommonParameters</span></span>
<span data-ttu-id="cecc4-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cecc4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cecc4-118">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cecc4-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cecc4-119">입력</span><span class="sxs-lookup"><span data-stu-id="cecc4-119">INPUTS</span></span>

### <span data-ttu-id="cecc4-120">없음</span><span class="sxs-lookup"><span data-stu-id="cecc4-120">None</span></span>

## <span data-ttu-id="cecc4-121">출력</span><span class="sxs-lookup"><span data-stu-id="cecc4-121">OUTPUTS</span></span>

### <span data-ttu-id="cecc4-122">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cecc4-122">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="cecc4-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cecc4-123">NOTES</span></span>

## <span data-ttu-id="cecc4-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cecc4-124">RELATED LINKS</span></span>

[<span data-ttu-id="cecc4-125">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="cecc4-125">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)

