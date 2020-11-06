---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/get-azurermsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalR.md
ms.openlocfilehash: 08e68a878267f706c280c8d461e8c904141cd06d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530883"
---
# <span data-ttu-id="4e43c-101">Get-AzureRmSignalR</span><span class="sxs-lookup"><span data-stu-id="4e43c-101">Get-AzureRmSignalR</span></span>

## <span data-ttu-id="4e43c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e43c-102">SYNOPSIS</span></span>
<span data-ttu-id="4e43c-103">특정 SignalR 서비스 또는 리소스 그룹 또는 구독에 있는 모든 SignalR 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4e43c-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e43c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4e43c-104">SYNTAX</span></span>

### <span data-ttu-id="4e43c-105">ListSignalRServiceParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4e43c-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzureRmSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e43c-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e43c-106">ResourceGroupParameterSet</span></span>
```
Get-AzureRmSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e43c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e43c-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e43c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4e43c-108">DESCRIPTION</span></span>
<span data-ttu-id="4e43c-109">특정 SignalR 서비스 또는 리소스 그룹 또는 구독에 있는 모든 SignalR 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4e43c-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="4e43c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4e43c-110">EXAMPLES</span></span>

### <span data-ttu-id="4e43c-111">구독에서 모든 SignalR 서비스 가져오기</span><span class="sxs-lookup"><span data-stu-id="4e43c-111">Get all SignalR services in the subscription</span></span>
```powershell
PS C:\> Get-AzureRmSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="4e43c-112">리소스 그룹에서 모든 SignalR 서비스 가져오기</span><span class="sxs-lookup"><span data-stu-id="4e43c-112">Get all SignalR services in a resource group</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="4e43c-113">특정 SignalR 서비스 받기</span><span class="sxs-lookup"><span data-stu-id="4e43c-113">Get a specific SignalR service</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="4e43c-114">기본 리소스 그룹에서 특정 SignalR 서비스 가져오기</span><span class="sxs-lookup"><span data-stu-id="4e43c-114">Get a specific SignalR service from the default resource group</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="4e43c-115">기본 리소스 그룹은을 (를) 설정할 수 있습니다 `Set-AzureRmDefault -ResourceGroupName myResourceGroup` .</span><span class="sxs-lookup"><span data-stu-id="4e43c-115">The default resource group can be set by `Set-AzureRmDefault -ResourceGroupName myResourceGroup`.</span></span>

## <span data-ttu-id="4e43c-116">변수</span><span class="sxs-lookup"><span data-stu-id="4e43c-116">PARAMETERS</span></span>

### <span data-ttu-id="4e43c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e43c-117">-DefaultProfile</span></span>
<span data-ttu-id="4e43c-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4e43c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e43c-119">-이름</span><span class="sxs-lookup"><span data-stu-id="4e43c-119">-Name</span></span>
<span data-ttu-id="4e43c-120">SignalR 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4e43c-120">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e43c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e43c-121">-ResourceGroupName</span></span>
<span data-ttu-id="4e43c-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4e43c-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListSignalRServiceParameterSet, ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e43c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e43c-123">-ResourceId</span></span>
<span data-ttu-id="4e43c-124">SignalR 서비스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4e43c-124">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e43c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e43c-125">CommonParameters</span></span>
<span data-ttu-id="4e43c-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e43c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e43c-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e43c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e43c-128">입력</span><span class="sxs-lookup"><span data-stu-id="4e43c-128">INPUTS</span></span>

### <span data-ttu-id="4e43c-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4e43c-129">System.String</span></span>
<span data-ttu-id="4e43c-130">매개 변수: ResourceId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4e43c-130">Parameters: ResourceId (ByValue)</span></span>

## <span data-ttu-id="4e43c-131">출력</span><span class="sxs-lookup"><span data-stu-id="4e43c-131">OUTPUTS</span></span>

### <span data-ttu-id="4e43c-132">SignalR. PSSignalRResource/.</span><span class="sxs-lookup"><span data-stu-id="4e43c-132">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="4e43c-133">상속자</span><span class="sxs-lookup"><span data-stu-id="4e43c-133">NOTES</span></span>

## <span data-ttu-id="4e43c-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4e43c-134">RELATED LINKS</span></span>
