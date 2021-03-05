---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: f4f2e76a9354ee6ed796b64cbdd83f21d70ff954
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978384"
---
# <span data-ttu-id="9876d-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span><span class="sxs-lookup"><span data-stu-id="9876d-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span></span>

## <span data-ttu-id="9876d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9876d-102">SYNOPSIS</span></span>
<span data-ttu-id="9876d-103">지원되는 서버 변수 및 사용 가능한 요청 및 응답 헤더를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9876d-103">Get the supported server variables and available request and response headers.</span></span>

## <span data-ttu-id="9876d-104">구문</span><span class="sxs-lookup"><span data-stu-id="9876d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## <span data-ttu-id="9876d-105">설명</span><span class="sxs-lookup"><span data-stu-id="9876d-105">DESCRIPTION</span></span>
<span data-ttu-id="9876d-106">**Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet은 지원되는 서버 변수 및 사용 가능한 요청 및 응답 헤더를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="9876d-106">The **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet gets the supported server variables and available request and response headers.</span></span> <span data-ttu-id="9876d-107">매개 변수를 사용하여 변수 또는 헤더 목록을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9876d-107">Parameters can be used to get the variables or headers lists.</span></span>

## <span data-ttu-id="9876d-108">예제</span><span class="sxs-lookup"><span data-stu-id="9876d-108">EXAMPLES</span></span>

### <span data-ttu-id="9876d-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="9876d-109">Example 1</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ServerVariable
```

<span data-ttu-id="9876d-110">이 명령은 사용 가능한 모든 서버 변수를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9876d-110">This commands returns all the available server variables.</span></span>

### <span data-ttu-id="9876d-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="9876d-111">Example 2</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -RequestHeader
```

<span data-ttu-id="9876d-112">이 명령은 사용 가능한 모든 요청 헤더를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9876d-112">This commands returns all the available request headers.</span></span>

### <span data-ttu-id="9876d-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="9876d-113">Example 3</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

<span data-ttu-id="9876d-114">이 명령은 사용 가능한 모든 응답 헤더를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9876d-114">This commands returns all the available response headers.</span></span>

### <span data-ttu-id="9876d-115">예제 4</span><span class="sxs-lookup"><span data-stu-id="9876d-115">Example 4</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader - ServerVariable -RequestHeader -ResponseHeader
```

<span data-ttu-id="9876d-116">이 명령은 사용 가능한 모든 서버 변수, 요청 및 응답 헤더를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9876d-116">This commands returns all the available server variables, request and response headers.</span></span>

### <span data-ttu-id="9876d-117">예제 5</span><span class="sxs-lookup"><span data-stu-id="9876d-117">Example 5</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader
```

<span data-ttu-id="9876d-118">이 명령은 사용 가능한 모든 서버 변수, 요청 및 응답 헤더를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9876d-118">This commands returns all the available server variables, request and response headers.</span></span>

## <span data-ttu-id="9876d-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9876d-119">PARAMETERS</span></span>

### <span data-ttu-id="9876d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9876d-120">-DefaultProfile</span></span>
<span data-ttu-id="9876d-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9876d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9876d-122">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="9876d-122">-RequestHeader</span></span>
<span data-ttu-id="9876d-123">Application Gateway 사용 가능한 요청 헤더.</span><span class="sxs-lookup"><span data-stu-id="9876d-123">Application Gateway available request headers.</span></span>

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

### <span data-ttu-id="9876d-124">-ResponseHeader</span><span class="sxs-lookup"><span data-stu-id="9876d-124">-ResponseHeader</span></span>
<span data-ttu-id="9876d-125">Application Gateway 사용 가능한 응답 헤더입니다.</span><span class="sxs-lookup"><span data-stu-id="9876d-125">Application Gateway available response headers.</span></span>

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

### <span data-ttu-id="9876d-126">-ServerVariable</span><span class="sxs-lookup"><span data-stu-id="9876d-126">-ServerVariable</span></span>
<span data-ttu-id="9876d-127">Application Gateway 사용 가능한 서버 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="9876d-127">Application Gateway available server variables.</span></span>

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

### <span data-ttu-id="9876d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9876d-128">CommonParameters</span></span>
<span data-ttu-id="9876d-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9876d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9876d-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9876d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9876d-131">입력</span><span class="sxs-lookup"><span data-stu-id="9876d-131">INPUTS</span></span>

### <span data-ttu-id="9876d-132">없음</span><span class="sxs-lookup"><span data-stu-id="9876d-132">None</span></span>

## <span data-ttu-id="9876d-133">출력</span><span class="sxs-lookup"><span data-stu-id="9876d-133">OUTPUTS</span></span>

### <span data-ttu-id="9876d-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span><span class="sxs-lookup"><span data-stu-id="9876d-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span></span>

## <span data-ttu-id="9876d-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9876d-135">NOTES</span></span>
<span data-ttu-id="9876d-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader는** **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet의 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="9876d-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** is an alias for the **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet.</span></span>

## <span data-ttu-id="9876d-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9876d-137">RELATED LINKS</span></span>
