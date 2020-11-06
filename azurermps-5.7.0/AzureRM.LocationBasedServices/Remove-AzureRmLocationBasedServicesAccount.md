---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/remove-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Remove-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Remove-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 0496fcdba082370654b3259f101987d1a78621fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532804"
---
# <span data-ttu-id="137a6-101">Remove-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="137a6-101">Remove-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="137a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="137a6-102">SYNOPSIS</span></span>
<span data-ttu-id="137a6-103">위치 기반 서비스 계정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="137a6-103">Deletes a Location Based Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="137a6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="137a6-104">SYNTAX</span></span>

### <span data-ttu-id="137a6-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="137a6-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="137a6-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="137a6-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="137a6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="137a6-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="137a6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="137a6-108">DESCRIPTION</span></span>
<span data-ttu-id="137a6-109">**AzureRmLocationBasedServicesAccount** cmdlet은 지정 된 위치 기반 서비스 계정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="137a6-109">The **Remove-AzureRmLocationBasedServicesAccount** cmdlet deletes the specified Location Based Services account.</span></span>

## <span data-ttu-id="137a6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="137a6-110">EXAMPLES</span></span>

### <span data-ttu-id="137a6-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="137a6-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="137a6-112">리소스 그룹 MyResourceGroup에서 계정 내 계정를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="137a6-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="137a6-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="137a6-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmLocationBasedServicesAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="137a6-114">지정 된 위치 기반 서비스 계정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="137a6-114">Deletes the specified Location Based Services Account.</span></span>

## <span data-ttu-id="137a6-115">변수</span><span class="sxs-lookup"><span data-stu-id="137a6-115">PARAMETERS</span></span>

### <span data-ttu-id="137a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="137a6-116">-DefaultProfile</span></span>
<span data-ttu-id="137a6-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="137a6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="137a6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="137a6-118">-InputObject</span></span>
<span data-ttu-id="137a6-119">Location 기반 서비스 계정이 [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md)에서 파이프 합니다.</span><span class="sxs-lookup"><span data-stu-id="137a6-119">Location Based Services Account piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span></span>

```yaml
Type: PSLocationBasedServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="137a6-120">-이름</span><span class="sxs-lookup"><span data-stu-id="137a6-120">-Name</span></span>
<span data-ttu-id="137a6-121">위치 기반 서비스 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="137a6-121">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="137a6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="137a6-122">-ResourceGroupName</span></span>
<span data-ttu-id="137a6-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="137a6-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="137a6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="137a6-124">-ResourceId</span></span>
<span data-ttu-id="137a6-125">위치 기반 서비스 계정 ResourceId.</span><span class="sxs-lookup"><span data-stu-id="137a6-125">Location Based Services Account ResourceId.</span></span>
```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="137a6-126">-확인</span><span class="sxs-lookup"><span data-stu-id="137a6-126">-Confirm</span></span>
<span data-ttu-id="137a6-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="137a6-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="137a6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="137a6-128">-WhatIf</span></span>
<span data-ttu-id="137a6-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="137a6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="137a6-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="137a6-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="137a6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="137a6-131">CommonParameters</span></span>
<span data-ttu-id="137a6-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="137a6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="137a6-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="137a6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="137a6-134">입력</span><span class="sxs-lookup"><span data-stu-id="137a6-134">INPUTS</span></span>

### <span data-ttu-id="137a6-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="137a6-135">System.String</span></span>

## <span data-ttu-id="137a6-136">출력</span><span class="sxs-lookup"><span data-stu-id="137a6-136">OUTPUTS</span></span>

### <span data-ttu-id="137a6-137">System. 개체</span><span class="sxs-lookup"><span data-stu-id="137a6-137">System.Object</span></span>

## <span data-ttu-id="137a6-138">상속자</span><span class="sxs-lookup"><span data-stu-id="137a6-138">NOTES</span></span>

## <span data-ttu-id="137a6-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="137a6-139">RELATED LINKS</span></span>
