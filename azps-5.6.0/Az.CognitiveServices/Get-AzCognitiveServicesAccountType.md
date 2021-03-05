---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
ms.openlocfilehash: aacc24926bf38f52f1fd273847e48082c8d110c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981216"
---
# <span data-ttu-id="4ec99-101">Get-AzCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="4ec99-101">Get-AzCognitiveServicesAccountType</span></span>

## <span data-ttu-id="4ec99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ec99-102">SYNOPSIS</span></span>
<span data-ttu-id="4ec99-103">사용 가능한 Cognitive Services 계정 유형을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4ec99-103">Gets the available Cognitive Services Account Types.</span></span>

## <span data-ttu-id="4ec99-104">구문</span><span class="sxs-lookup"><span data-stu-id="4ec99-104">SYNTAX</span></span>

### <span data-ttu-id="4ec99-105">GetAccountTypes(기본값)</span><span class="sxs-lookup"><span data-stu-id="4ec99-105">GetAccountTypes (Default)</span></span>
```
Get-AzCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4ec99-106">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="4ec99-106">GetAccountTypeWithName</span></span>
```
Get-AzCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ec99-107">설명</span><span class="sxs-lookup"><span data-stu-id="4ec99-107">DESCRIPTION</span></span>
<span data-ttu-id="4ec99-108">**Get-AzCognitiveServicesAccountType** cmdlet은 이 구독 아래에서 사용할 수 있는 Cognitive Services 계정 유형을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4ec99-108">The **Get-AzCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="4ec99-109">예제</span><span class="sxs-lookup"><span data-stu-id="4ec99-109">EXAMPLES</span></span>

### <span data-ttu-id="4ec99-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="4ec99-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType
```

<span data-ttu-id="4ec99-111">사용 가능한 형식의 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4ec99-111">Get the list of available Types.</span></span>

### <span data-ttu-id="4ec99-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="4ec99-112">Example 2</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="4ec99-113">westus에서 사용 가능한 형식의 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4ec99-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="4ec99-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="4ec99-114">Example 3</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="4ec99-115">유효한 형식 이름인 경우 유효한 이름인 경우 이름이 `Face` 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ec99-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="4ec99-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4ec99-116">PARAMETERS</span></span>

### <span data-ttu-id="4ec99-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ec99-117">-DefaultProfile</span></span>
<span data-ttu-id="4ec99-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4ec99-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ec99-119">-Location</span><span class="sxs-lookup"><span data-stu-id="4ec99-119">-Location</span></span>
<span data-ttu-id="4ec99-120">Cognitive Services 계정 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4ec99-120">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="4ec99-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="4ec99-121">-TypeName</span></span>
<span data-ttu-id="4ec99-122">Cognitive Services 계정 유형 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ec99-122">Cognitive Services Account Type Name.</span></span>

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

### <span data-ttu-id="4ec99-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ec99-123">CommonParameters</span></span>
<span data-ttu-id="4ec99-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4ec99-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ec99-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ec99-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ec99-126">입력</span><span class="sxs-lookup"><span data-stu-id="4ec99-126">INPUTS</span></span>

### <span data-ttu-id="4ec99-127">System.String</span><span class="sxs-lookup"><span data-stu-id="4ec99-127">System.String</span></span>

## <span data-ttu-id="4ec99-128">출력</span><span class="sxs-lookup"><span data-stu-id="4ec99-128">OUTPUTS</span></span>

### <span data-ttu-id="4ec99-129">System.String[]</span><span class="sxs-lookup"><span data-stu-id="4ec99-129">System.String[]</span></span>

### <span data-ttu-id="4ec99-130">System.String</span><span class="sxs-lookup"><span data-stu-id="4ec99-130">System.String</span></span>

## <span data-ttu-id="4ec99-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4ec99-131">NOTES</span></span>

## <span data-ttu-id="4ec99-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ec99-132">RELATED LINKS</span></span>
