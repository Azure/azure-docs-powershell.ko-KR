---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 696ae59cb5115181605b7e6e647e2eb7d2792fd8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333170"
---
# <span data-ttu-id="6a239-101">Get-AzAccessToken</span><span class="sxs-lookup"><span data-stu-id="6a239-101">Get-AzAccessToken</span></span>

## <span data-ttu-id="6a239-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a239-102">SYNOPSIS</span></span>
<span data-ttu-id="6a239-103">원시 액세스 토큰을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6a239-103">Get raw access token.</span></span> <span data-ttu-id="6a239-104">-ResourceUrl을 사용하는 경우 값이 현재 Azure 환경과 일치하는지 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="6a239-104">When using -ResourceUrl, please make sure the value does match current Azure environment.</span></span> <span data-ttu-id="6a239-105">.의 값을 참조할 수 `(Get-AzContext).Environment` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a239-105">You may refer to the value of `(Get-AzContext).Environment`.</span></span>

## <span data-ttu-id="6a239-106">구문</span><span class="sxs-lookup"><span data-stu-id="6a239-106">SYNTAX</span></span>

### <span data-ttu-id="6a239-107">KnownResourceTypeName(기본값)</span><span class="sxs-lookup"><span data-stu-id="6a239-107">KnownResourceTypeName (Default)</span></span>
```
Get-AzAccessToken [-ResourceTypeName <String>] [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6a239-108">ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="6a239-108">ResourceUrl</span></span>
```
Get-AzAccessToken -ResourceUrl <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a239-109">설명</span><span class="sxs-lookup"><span data-stu-id="6a239-109">DESCRIPTION</span></span>
<span data-ttu-id="6a239-110">액세스 토큰을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a239-110">Get access token</span></span>

## <span data-ttu-id="6a239-111">예제</span><span class="sxs-lookup"><span data-stu-id="6a239-111">EXAMPLES</span></span>

### <span data-ttu-id="6a239-112">예제 1 엔드포인트에 대한 원시 ARM 토큰을 얻음</span><span class="sxs-lookup"><span data-stu-id="6a239-112">Example 1 Get raw access token for ARM endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken
```

<span data-ttu-id="6a239-113">현재 계정에 대한 ResourceManager 엔드포인트의 액세스 토큰을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a239-113">Get access token of ResourceManager endpoint for current account</span></span>

### <span data-ttu-id="6a239-114">예제 2 AAD 그래프 엔드포인트에 대한 원시 액세스 토큰을 얻게</span><span class="sxs-lookup"><span data-stu-id="6a239-114">Example 2 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

<span data-ttu-id="6a239-115">현재 계정에 대한 AAD 그래프 엔드포인트의 액세스 토큰을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a239-115">Get access token of AAD graph endpoint for current account</span></span>

### <span data-ttu-id="6a239-116">예제 3 AAD 그래프 엔드포인트에 대한 원시 액세스 토큰을 얻게</span><span class="sxs-lookup"><span data-stu-id="6a239-116">Example 3 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

<span data-ttu-id="6a239-117">현재 계정에 대한 AAD 그래프 엔드포인트의 액세스 토큰을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a239-117">Get access token of AAD graph endpoint for current account</span></span>

## <span data-ttu-id="6a239-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a239-118">PARAMETERS</span></span>

### <span data-ttu-id="6a239-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a239-119">-DefaultProfile</span></span>
<span data-ttu-id="6a239-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6a239-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a239-121">-ResourceTypeName</span><span class="sxs-lookup"><span data-stu-id="6a239-121">-ResourceTypeName</span></span>
<span data-ttu-id="6a239-122">선택적 리소스 유형 이름, 지원되는 값: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse.</span><span class="sxs-lookup"><span data-stu-id="6a239-122">Optional resouce type name, supported values: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse.</span></span> <span data-ttu-id="6a239-123">기본값은 지정되지 않은 경우 Arm입니다.</span><span class="sxs-lookup"><span data-stu-id="6a239-123">Default value is Arm if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: KnownResourceTypeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a239-124">-ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="6a239-124">-ResourceUrl</span></span>
<span data-ttu-id="6a239-125">토큰을 요청하는 리소스 URL(예: http://graph.windows.net/ '.</span><span class="sxs-lookup"><span data-stu-id="6a239-125">Resource url for that you're requesting token, e.g. 'http://graph.windows.net/'.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUrl
Aliases: Resource, ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a239-126">-TenantId</span><span class="sxs-lookup"><span data-stu-id="6a239-126">-TenantId</span></span>
<span data-ttu-id="6a239-127">선택적 테넌트 ID입니다. 지정되지 않은 경우 기본 컨텍스트의 테넌트 ID를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a239-127">Optional Tenant Id. Use tenant id of default context if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a239-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a239-128">CommonParameters</span></span>
<span data-ttu-id="6a239-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6a239-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a239-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6a239-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a239-131">입력</span><span class="sxs-lookup"><span data-stu-id="6a239-131">INPUTS</span></span>

### <span data-ttu-id="6a239-132">없음</span><span class="sxs-lookup"><span data-stu-id="6a239-132">None</span></span>

## <span data-ttu-id="6a239-133">출력</span><span class="sxs-lookup"><span data-stu-id="6a239-133">OUTPUTS</span></span>

### <span data-ttu-id="6a239-134">System.String</span><span class="sxs-lookup"><span data-stu-id="6a239-134">System.String</span></span>

## <span data-ttu-id="6a239-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6a239-135">NOTES</span></span>

## <span data-ttu-id="6a239-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6a239-136">RELATED LINKS</span></span>
