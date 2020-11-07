---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: 8f0fc8caba03251ede507fc383ef99c10a06eeb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700669"
---
# <span data-ttu-id="685bf-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span><span class="sxs-lookup"><span data-stu-id="685bf-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span></span>

## <span data-ttu-id="685bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="685bf-102">SYNOPSIS</span></span>
<span data-ttu-id="685bf-103">지원 되는 서버 변수 및 사용 가능한 요청 및 응답 헤더를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="685bf-103">Get the supported server variables and available request and response headers.</span></span>

## <span data-ttu-id="685bf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="685bf-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## <span data-ttu-id="685bf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="685bf-105">DESCRIPTION</span></span>
<span data-ttu-id="685bf-106">**AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet은 지원 되는 서버 변수 및 사용 가능한 요청 및 응답 헤더를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="685bf-106">The **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet gets the supported server variables and available request and response headers.</span></span> <span data-ttu-id="685bf-107">매개 변수를 사용 하 여 변수 또는 헤더 목록을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="685bf-107">Parameters can be used to get the variables or headers lists.</span></span>

## <span data-ttu-id="685bf-108">예제의</span><span class="sxs-lookup"><span data-stu-id="685bf-108">EXAMPLES</span></span>

### <span data-ttu-id="685bf-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="685bf-109">Example 1</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ServerVariable
```

<span data-ttu-id="685bf-110">이 명령은 사용 가능한 모든 서버 변수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="685bf-110">This commands returns all the available server variables.</span></span>

### <span data-ttu-id="685bf-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="685bf-111">Example 2</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -RequestHeader
```

<span data-ttu-id="685bf-112">이 명령은 사용 가능한 모든 요청 헤더를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="685bf-112">This commands returns all the available request headers.</span></span>

### <span data-ttu-id="685bf-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="685bf-113">Example 3</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

<span data-ttu-id="685bf-114">이 명령은 사용 가능한 모든 응답 헤더를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="685bf-114">This commands returns all the available response headers.</span></span>

### <span data-ttu-id="685bf-115">예제 4</span><span class="sxs-lookup"><span data-stu-id="685bf-115">Example 4</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader - ServerVariable -RequestHeader -ResponseHeader
```

<span data-ttu-id="685bf-116">이 명령은 사용 가능한 모든 서버 변수, 요청 및 응답 헤더를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="685bf-116">This commands returns all the available server variables, request and response headers.</span></span>

### <span data-ttu-id="685bf-117">예제 5</span><span class="sxs-lookup"><span data-stu-id="685bf-117">Example 5</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader
```

<span data-ttu-id="685bf-118">이 명령은 사용 가능한 모든 서버 변수, 요청 및 응답 헤더를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="685bf-118">This commands returns all the available server variables, request and response headers.</span></span>

## <span data-ttu-id="685bf-119">변수</span><span class="sxs-lookup"><span data-stu-id="685bf-119">PARAMETERS</span></span>

### <span data-ttu-id="685bf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="685bf-120">-DefaultProfile</span></span>
<span data-ttu-id="685bf-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="685bf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="685bf-122">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="685bf-122">-RequestHeader</span></span>
<span data-ttu-id="685bf-123">응용 프로그램 게이트웨이 사용 가능한 요청 헤더.</span><span class="sxs-lookup"><span data-stu-id="685bf-123">Application Gateway available request headers.</span></span>

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

### <span data-ttu-id="685bf-124">-ResponseHeader</span><span class="sxs-lookup"><span data-stu-id="685bf-124">-ResponseHeader</span></span>
<span data-ttu-id="685bf-125">Application Gateway 사용 가능한 응답 헤더.</span><span class="sxs-lookup"><span data-stu-id="685bf-125">Application Gateway available response headers.</span></span>

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

### <span data-ttu-id="685bf-126">-ServerVariable</span><span class="sxs-lookup"><span data-stu-id="685bf-126">-ServerVariable</span></span>
<span data-ttu-id="685bf-127">Application Gateway 사용 가능한 서버 변수</span><span class="sxs-lookup"><span data-stu-id="685bf-127">Application Gateway available server variables.</span></span>

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

### <span data-ttu-id="685bf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="685bf-128">CommonParameters</span></span>
<span data-ttu-id="685bf-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="685bf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="685bf-130">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="685bf-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="685bf-131">입력</span><span class="sxs-lookup"><span data-stu-id="685bf-131">INPUTS</span></span>

### <span data-ttu-id="685bf-132">않아야</span><span class="sxs-lookup"><span data-stu-id="685bf-132">None</span></span>

## <span data-ttu-id="685bf-133">출력</span><span class="sxs-lookup"><span data-stu-id="685bf-133">OUTPUTS</span></span>

### <span data-ttu-id="685bf-134">PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="685bf-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span></span>

## <span data-ttu-id="685bf-135">상속자</span><span class="sxs-lookup"><span data-stu-id="685bf-135">NOTES</span></span>
<span data-ttu-id="685bf-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** 는 **AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet에 대 한 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="685bf-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** is an alias for the **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet.</span></span>

## <span data-ttu-id="685bf-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="685bf-137">RELATED LINKS</span></span>
