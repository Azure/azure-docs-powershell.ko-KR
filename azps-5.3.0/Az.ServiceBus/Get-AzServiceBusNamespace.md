---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
ms.openlocfilehash: 359ff0ce6de0c017d1ea2a65adc1d4573e45c17f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494891"
---
# <span data-ttu-id="417b3-101">Get-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="417b3-101">Get-AzServiceBusNamespace</span></span>

## <span data-ttu-id="417b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="417b3-102">SYNOPSIS</span></span>
<span data-ttu-id="417b3-103">리소스 그룹 내에서 지정된 Service Bus 네임스페이스에 대한 설명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="417b3-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="417b3-104">구문</span><span class="sxs-lookup"><span data-stu-id="417b3-104">SYNTAX</span></span>

```
Get-AzServiceBusNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="417b3-105">설명</span><span class="sxs-lookup"><span data-stu-id="417b3-105">DESCRIPTION</span></span>
<span data-ttu-id="417b3-106">**Get-AzServiceBusNamespace** cmdlet은 리소스 그룹 내에서 지정된 Service Bus 네임스페이스에 대한 설명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="417b3-106">The **Get-AzServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="417b3-107">예제</span><span class="sxs-lookup"><span data-stu-id="417b3-107">EXAMPLES</span></span>

### <span data-ttu-id="417b3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="417b3-108">Example 1</span></span>

```
PS C:\> Get-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 1:40:01 AM
UpdatedAt          : 1/20/2017 1:40:24 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

## <span data-ttu-id="417b3-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="417b3-109">PARAMETERS</span></span>

### <span data-ttu-id="417b3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="417b3-110">-DefaultProfile</span></span>
<span data-ttu-id="417b3-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="417b3-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="417b3-112">-Name</span><span class="sxs-lookup"><span data-stu-id="417b3-112">-Name</span></span>
<span data-ttu-id="417b3-113">네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="417b3-113">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="417b3-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="417b3-114">-ResourceGroupName</span></span>
<span data-ttu-id="417b3-115">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="417b3-115">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="417b3-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="417b3-116">CommonParameters</span></span>
<span data-ttu-id="417b3-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="417b3-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="417b3-118">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="417b3-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="417b3-119">입력</span><span class="sxs-lookup"><span data-stu-id="417b3-119">INPUTS</span></span>

### <span data-ttu-id="417b3-120">System.String</span><span class="sxs-lookup"><span data-stu-id="417b3-120">System.String</span></span>

## <span data-ttu-id="417b3-121">출력</span><span class="sxs-lookup"><span data-stu-id="417b3-121">OUTPUTS</span></span>

### <span data-ttu-id="417b3-122">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="417b3-122">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="417b3-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="417b3-123">NOTES</span></span>

## <span data-ttu-id="417b3-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="417b3-124">RELATED LINKS</span></span>
