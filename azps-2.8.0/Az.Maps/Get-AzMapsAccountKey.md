---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/get-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
ms.openlocfilehash: d4523dc240c015f4dea29b86e1285a9fce9afbc2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689381"
---
# <span data-ttu-id="f7dcb-101">Get-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="f7dcb-101">Get-AzMapsAccountKey</span></span>

## <span data-ttu-id="f7dcb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7dcb-102">SYNOPSIS</span></span>
<span data-ttu-id="f7dcb-103">계정에 대 한 API 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f7dcb-103">Gets the API keys for an account.</span></span>
<span data-ttu-id="f7dcb-104">이러한 키는 Azure Maps에 대 한 후속 호출에 사용 되는 인증 메커니즘입니다.</span><span class="sxs-lookup"><span data-stu-id="f7dcb-104">These keys are the authentication mechanism used in subsequent calls to Azure Maps.</span></span>

## <span data-ttu-id="f7dcb-105">구문과</span><span class="sxs-lookup"><span data-stu-id="f7dcb-105">SYNTAX</span></span>

### <span data-ttu-id="f7dcb-106">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f7dcb-106">NameParameterSet (Default)</span></span>
```
Get-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7dcb-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7dcb-107">InputObjectParameterSet</span></span>
```
Get-AzMapsAccountKey [-InputObject <PSMapsAccount>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7dcb-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7dcb-108">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7dcb-109">설명은</span><span class="sxs-lookup"><span data-stu-id="f7dcb-109">DESCRIPTION</span></span>
<span data-ttu-id="f7dcb-110">Get-AzMapsAccountKey cmdlet은 프로 비전 된 Azure Maps 계정에 대 한 API 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f7dcb-110">The Get-AzMapsAccountKey cmdlet gets the API keys for a provisioned Azure Maps account.</span></span>
<span data-ttu-id="f7dcb-111">Azure Maps 계정에는 기본 및 보조의 두 가지 API 키가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f7dcb-111">An Azure Maps account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="f7dcb-112">키를 사용 하 여 Azure Maps 계정 끝점과 상호 작용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f7dcb-112">The keys enable interaction with the Azure Maps account endpoint.</span></span>
<span data-ttu-id="f7dcb-113">New-AzMapsAccountKey (New-AzMapsAccountKey)를 사용 하 여 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7dcb-113">Use New-AzMapsAccountKey (New-AzMapsAccountKey.md)to regenerate a key.</span></span>

## <span data-ttu-id="f7dcb-114">예제의</span><span class="sxs-lookup"><span data-stu-id="f7dcb-114">EXAMPLES</span></span>

### <span data-ttu-id="f7dcb-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="f7dcb-115">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="f7dcb-116">리소스 그룹 MyResourceGroup의 내 계정 이라는 계정에 대 한 키를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7dcb-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="f7dcb-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="f7dcb-117">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="f7dcb-118">지정 된 Azure Maps 계정에 대 한 키를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7dcb-118">Returns the keys for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="f7dcb-119">변수</span><span class="sxs-lookup"><span data-stu-id="f7dcb-119">PARAMETERS</span></span>

### <span data-ttu-id="f7dcb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7dcb-120">-DefaultProfile</span></span>
<span data-ttu-id="f7dcb-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f7dcb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7dcb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7dcb-122">-InputObject</span></span>
<span data-ttu-id="f7dcb-123">AzMapsAccount에서 파이프 맵 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f7dcb-123">Maps Account piped from Get-AzMapsAccount.</span></span>

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

### <span data-ttu-id="f7dcb-124">-이름</span><span class="sxs-lookup"><span data-stu-id="f7dcb-124">-Name</span></span>
<span data-ttu-id="f7dcb-125">계정 이름을 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="f7dcb-125">Maps Account Name.</span></span>

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

### <span data-ttu-id="f7dcb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7dcb-126">-ResourceGroupName</span></span>
<span data-ttu-id="f7dcb-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f7dcb-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="f7dcb-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7dcb-128">-ResourceId</span></span>
<span data-ttu-id="f7dcb-129">Maps 계정 ResourceId.</span><span class="sxs-lookup"><span data-stu-id="f7dcb-129">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="f7dcb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7dcb-130">CommonParameters</span></span>
<span data-ttu-id="f7dcb-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7dcb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7dcb-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7dcb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7dcb-133">입력</span><span class="sxs-lookup"><span data-stu-id="f7dcb-133">INPUTS</span></span>

### <span data-ttu-id="f7dcb-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f7dcb-134">System.String</span></span>

### <span data-ttu-id="f7dcb-135">Microsoft Azure. \*. \*. \*.</span><span class="sxs-lookup"><span data-stu-id="f7dcb-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="f7dcb-136">출력</span><span class="sxs-lookup"><span data-stu-id="f7dcb-136">OUTPUTS</span></span>

### <span data-ttu-id="f7dcb-137">Microsoft. \*. \*. \*. \*.</span><span class="sxs-lookup"><span data-stu-id="f7dcb-137">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span></span>

## <span data-ttu-id="f7dcb-138">상속자</span><span class="sxs-lookup"><span data-stu-id="f7dcb-138">NOTES</span></span>

## <span data-ttu-id="f7dcb-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f7dcb-139">RELATED LINKS</span></span>