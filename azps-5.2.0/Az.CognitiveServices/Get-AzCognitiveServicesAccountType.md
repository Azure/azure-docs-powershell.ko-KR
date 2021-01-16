---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
ms.openlocfilehash: a99ca4bb636ba1767fc5f50611d3c5a9eb991312
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338541"
---
# <span data-ttu-id="48b91-101">Get-AzCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="48b91-101">Get-AzCognitiveServicesAccountType</span></span>

## <span data-ttu-id="48b91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48b91-102">SYNOPSIS</span></span>
<span data-ttu-id="48b91-103">사용 가능한 Cognitive Services 계정 유형을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="48b91-103">Gets the available Cognitive Services Account Types.</span></span>

## <span data-ttu-id="48b91-104">구문</span><span class="sxs-lookup"><span data-stu-id="48b91-104">SYNTAX</span></span>

### <span data-ttu-id="48b91-105">GetAccountTypes(기본값)</span><span class="sxs-lookup"><span data-stu-id="48b91-105">GetAccountTypes (Default)</span></span>
```
Get-AzCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="48b91-106">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="48b91-106">GetAccountTypeWithName</span></span>
```
Get-AzCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="48b91-107">설명</span><span class="sxs-lookup"><span data-stu-id="48b91-107">DESCRIPTION</span></span>
<span data-ttu-id="48b91-108">**Get-AzCognitiveServicesAccountType** cmdlet은 이 구독에서 사용 가능한 Cognitive Services 계정 유형을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="48b91-108">The **Get-AzCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="48b91-109">예제</span><span class="sxs-lookup"><span data-stu-id="48b91-109">EXAMPLES</span></span>

### <span data-ttu-id="48b91-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="48b91-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType
```

<span data-ttu-id="48b91-111">사용 가능한 형식 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="48b91-111">Get the list of available Types.</span></span>

### <span data-ttu-id="48b91-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="48b91-112">Example 2</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="48b91-113">westus에서 사용 가능한 형식 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="48b91-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="48b91-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="48b91-114">Example 3</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="48b91-115">유효한 형식 이름이 유효한지 확인한 후 유효한 이름인 경우 `Face` 이름이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="48b91-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="48b91-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48b91-116">PARAMETERS</span></span>

### <span data-ttu-id="48b91-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48b91-117">-DefaultProfile</span></span>
<span data-ttu-id="48b91-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="48b91-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48b91-119">-Location</span><span class="sxs-lookup"><span data-stu-id="48b91-119">-Location</span></span>
<span data-ttu-id="48b91-120">Cognitive Services 계정 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="48b91-120">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAccountTypes
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48b91-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="48b91-121">-TypeName</span></span>
<span data-ttu-id="48b91-122">Cognitive Services 계정 유형 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="48b91-122">Cognitive Services Account Type Name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAccountTypeWithName
Aliases: CognitiveServicesAccountTypeName, AccountTypeName, KindName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48b91-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48b91-123">CommonParameters</span></span>
<span data-ttu-id="48b91-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="48b91-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48b91-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="48b91-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48b91-126">입력</span><span class="sxs-lookup"><span data-stu-id="48b91-126">INPUTS</span></span>

### <span data-ttu-id="48b91-127">System.String</span><span class="sxs-lookup"><span data-stu-id="48b91-127">System.String</span></span>

## <span data-ttu-id="48b91-128">출력</span><span class="sxs-lookup"><span data-stu-id="48b91-128">OUTPUTS</span></span>

### <span data-ttu-id="48b91-129">System.String[]</span><span class="sxs-lookup"><span data-stu-id="48b91-129">System.String[]</span></span>

### <span data-ttu-id="48b91-130">System.String</span><span class="sxs-lookup"><span data-stu-id="48b91-130">System.String</span></span>

## <span data-ttu-id="48b91-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="48b91-131">NOTES</span></span>

## <span data-ttu-id="48b91-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="48b91-132">RELATED LINKS</span></span>
