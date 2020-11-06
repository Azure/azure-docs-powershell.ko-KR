---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/new-azurermlocationbasedservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccountKey.md
ms.openlocfilehash: 7116cd4c5da2dd897af4e6540593a5e5458e4eda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529800"
---
# <span data-ttu-id="3745d-101">New-AzureRmLocationBasedServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="3745d-101">New-AzureRmLocationBasedServicesAccountKey</span></span>

## <span data-ttu-id="3745d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3745d-102">SYNOPSIS</span></span>
<span data-ttu-id="3745d-103">계정 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3745d-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3745d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3745d-104">SYNTAX</span></span>

### <span data-ttu-id="3745d-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3745d-105">NameParameterSet (Default)</span></span>
```
New-AzureRmLocationBasedServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3745d-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3745d-106">InputObjectParameterSet</span></span>
```
New-AzureRmLocationBasedServicesAccountKey [-KeyName] <String> [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3745d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3745d-107">ResourceIdParameterSet</span></span>
```
New-AzureRmLocationBasedServicesAccountKey [-KeyName] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3745d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3745d-108">DESCRIPTION</span></span>
<span data-ttu-id="3745d-109">**AzureRmLocationBasedServicesAccountKey** Cmdlet은 위치 기반 서비스 계정에 대 한 API 키를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3745d-109">The **New-AzureRmLocationBasedServicesAccountKey** cmdlet regenerates an API key for a Location Based Services account.</span></span>

## <span data-ttu-id="3745d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3745d-110">EXAMPLES</span></span>

### <span data-ttu-id="3745d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3745d-111">Example 1</span></span>
```
PS C:\> New-AzureRmLocationBasedServicesAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount -KeyName Primary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Primary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="3745d-112">리소스 그룹 MyResourceGroup의 계정 내 계정에 대 한 기본 API 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3745d-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="3745d-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="3745d-113">Example 2</span></span>
```
PS C:\> New-AzureRmLocationBasedServicesAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount -KeyName Secondary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Secondary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="3745d-114">지정 된 위치 기반 서비스 계정에 대 한 보조 API 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3745d-114">Regenerates the Secondary API Key for the specified Location Based Services Account.</span></span>

## <span data-ttu-id="3745d-115">변수</span><span class="sxs-lookup"><span data-stu-id="3745d-115">PARAMETERS</span></span>

### <span data-ttu-id="3745d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3745d-116">-DefaultProfile</span></span>
<span data-ttu-id="3745d-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3745d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3745d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3745d-118">-InputObject</span></span>
<span data-ttu-id="3745d-119">Location 기반 서비스 계정이 [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md)에서 파이프 합니다.</span><span class="sxs-lookup"><span data-stu-id="3745d-119">Location Based Services Account piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span></span>

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

### <span data-ttu-id="3745d-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="3745d-120">-KeyName</span></span>
<span data-ttu-id="3745d-121">위치 기반 서비스 계정 키.</span><span class="sxs-lookup"><span data-stu-id="3745d-121">Location Based Services Account Key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3745d-122">-이름</span><span class="sxs-lookup"><span data-stu-id="3745d-122">-Name</span></span>
<span data-ttu-id="3745d-123">위치 기반 서비스 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3745d-123">Location Based Services Account Name.</span></span>

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

### <span data-ttu-id="3745d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3745d-124">-ResourceGroupName</span></span>
<span data-ttu-id="3745d-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3745d-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="3745d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3745d-126">-ResourceId</span></span>
<span data-ttu-id="3745d-127">위치 기반 서비스 계정 ResourceId.</span><span class="sxs-lookup"><span data-stu-id="3745d-127">Location Based Services Account ResourceId.</span></span>
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

### <span data-ttu-id="3745d-128">-확인</span><span class="sxs-lookup"><span data-stu-id="3745d-128">-Confirm</span></span>
<span data-ttu-id="3745d-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3745d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3745d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3745d-130">-WhatIf</span></span>
<span data-ttu-id="3745d-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3745d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3745d-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3745d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3745d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3745d-133">CommonParameters</span></span>
<span data-ttu-id="3745d-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3745d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3745d-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3745d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3745d-136">입력</span><span class="sxs-lookup"><span data-stu-id="3745d-136">INPUTS</span></span>

### <span data-ttu-id="3745d-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3745d-137">System.String</span></span>
<span data-ttu-id="3745d-138">LocationBasedServices. NewAzureLocationBasedServicesAccountKeyCommand + KeyNameType</span><span class="sxs-lookup"><span data-stu-id="3745d-138">Microsoft.Azure.Commands.LocationBasedServices.NewAzureLocationBasedServicesAccountKeyCommand+KeyNameType</span></span>

## <span data-ttu-id="3745d-139">출력</span><span class="sxs-lookup"><span data-stu-id="3745d-139">OUTPUTS</span></span>

### <span data-ttu-id="3745d-140">LocationBasedServices. LocationBasedServicesAccountKeys/.</span><span class="sxs-lookup"><span data-stu-id="3745d-140">Microsoft.Azure.Management.LocationBasedServices.Models.LocationBasedServicesAccountKeys</span></span>

## <span data-ttu-id="3745d-141">상속자</span><span class="sxs-lookup"><span data-stu-id="3745d-141">NOTES</span></span>

## <span data-ttu-id="3745d-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3745d-142">RELATED LINKS</span></span>
