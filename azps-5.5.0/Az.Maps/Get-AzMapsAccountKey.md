---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/get-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
ms.openlocfilehash: 4969ba5cdb8b24627e620b82a13806c7b4cc687e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187449"
---
# <span data-ttu-id="3f749-101">Get-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="3f749-101">Get-AzMapsAccountKey</span></span>

## <span data-ttu-id="3f749-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f749-102">SYNOPSIS</span></span>
<span data-ttu-id="3f749-103">계정에 대한 API 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3f749-103">Gets the API keys for an account.</span></span>
<span data-ttu-id="3f749-104">이러한 키는 Azure Maps에 대한 후속 호출에 사용되는 인증 메커니즘입니다.</span><span class="sxs-lookup"><span data-stu-id="3f749-104">These keys are the authentication mechanism used in subsequent calls to Azure Maps.</span></span>

## <span data-ttu-id="3f749-105">구문</span><span class="sxs-lookup"><span data-stu-id="3f749-105">SYNTAX</span></span>

### <span data-ttu-id="3f749-106">NameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3f749-106">NameParameterSet (Default)</span></span>
```
Get-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f749-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f749-107">InputObjectParameterSet</span></span>
```
Get-AzMapsAccountKey [-InputObject <PSMapsAccount>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f749-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f749-108">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f749-109">설명</span><span class="sxs-lookup"><span data-stu-id="3f749-109">DESCRIPTION</span></span>
<span data-ttu-id="3f749-110">Get-AzMapsAccountKey cmdlet은 프로비전된 Azure Maps 계정에 대한 API 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3f749-110">The Get-AzMapsAccountKey cmdlet gets the API keys for a provisioned Azure Maps account.</span></span>
<span data-ttu-id="3f749-111">Azure Maps 계정에는 기본 키와 보조 키의 두 개의 API 키가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3f749-111">An Azure Maps account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="3f749-112">키를 사용하면 Azure Maps 계정 엔드포인트와 상호 작용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3f749-112">The keys enable interaction with the Azure Maps account endpoint.</span></span>
<span data-ttu-id="3f749-113">키 New-AzMapsAccountKey(New-AzMapsAccountKey.md)를 사용하여 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="3f749-113">Use New-AzMapsAccountKey (New-AzMapsAccountKey.md)to regenerate a key.</span></span>

## <span data-ttu-id="3f749-114">예제</span><span class="sxs-lookup"><span data-stu-id="3f749-114">EXAMPLES</span></span>

### <span data-ttu-id="3f749-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="3f749-115">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="3f749-116">리소스 그룹 MyResourceGroup에서 MyAccount라는 계정에 대한 키를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3f749-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="3f749-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="3f749-117">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="3f749-118">지정된 Azure Maps 계정에 대한 키를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3f749-118">Returns the keys for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="3f749-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f749-119">PARAMETERS</span></span>

### <span data-ttu-id="3f749-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f749-120">-DefaultProfile</span></span>
<span data-ttu-id="3f749-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3f749-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f749-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f749-122">-InputObject</span></span>
<span data-ttu-id="3f749-123">Get-AzMapsAccount에서 파이프된 Maps 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="3f749-123">Maps Account piped from Get-AzMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f749-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3f749-124">-Name</span></span>
<span data-ttu-id="3f749-125">계정 이름을 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="3f749-125">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f749-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f749-126">-ResourceGroupName</span></span>
<span data-ttu-id="3f749-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f749-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f749-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f749-128">-ResourceId</span></span>
<span data-ttu-id="3f749-129">계정 ResourceId를 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="3f749-129">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f749-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f749-130">CommonParameters</span></span>
<span data-ttu-id="3f749-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3f749-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f749-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3f749-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f749-133">입력</span><span class="sxs-lookup"><span data-stu-id="3f749-133">INPUTS</span></span>

### <span data-ttu-id="3f749-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3f749-134">System.String</span></span>

### <span data-ttu-id="3f749-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="3f749-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="3f749-136">출력</span><span class="sxs-lookup"><span data-stu-id="3f749-136">OUTPUTS</span></span>

### <span data-ttu-id="3f749-137">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="3f749-137">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span></span>

## <span data-ttu-id="3f749-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3f749-138">NOTES</span></span>

## <span data-ttu-id="3f749-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f749-139">RELATED LINKS</span></span>
