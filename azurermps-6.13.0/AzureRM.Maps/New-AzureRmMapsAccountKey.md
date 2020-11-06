---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/new-azurermmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/New-AzureRmMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/New-AzureRmMapsAccountKey.md
ms.openlocfilehash: 13364cde6799a6d99bcdba1d5cd2078c3392a2cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530915"
---
# <span data-ttu-id="378bc-101">New-AzureRmMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="378bc-101">New-AzureRmMapsAccountKey</span></span>

## <span data-ttu-id="378bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="378bc-102">SYNOPSIS</span></span>
<span data-ttu-id="378bc-103">계정 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="378bc-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="378bc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="378bc-104">SYNTAX</span></span>

### <span data-ttu-id="378bc-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="378bc-105">NameParameterSet (Default)</span></span>
```
New-AzureRmMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="378bc-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="378bc-106">InputObjectParameterSet</span></span>
```
New-AzureRmMapsAccountKey [-KeyName] <String> [-InputObject <PSMapsAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="378bc-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="378bc-107">ResourceIdParameterSet</span></span>
```
New-AzureRmMapsAccountKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="378bc-108">설명은</span><span class="sxs-lookup"><span data-stu-id="378bc-108">DESCRIPTION</span></span>
<span data-ttu-id="378bc-109">New-AzureRmMapsAccountKey cmdlet은 Azure Maps 계정에 대 한 API 키를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="378bc-109">The New-AzureRmMapsAccountKey cmdlet regenerates an API key for a Azure Maps account.</span></span>

## <span data-ttu-id="378bc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="378bc-110">EXAMPLES</span></span>

### <span data-ttu-id="378bc-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="378bc-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount -KeyName Primary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Primary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="378bc-112">리소스 그룹 MyResourceGroup의 계정 내 계정에 대 한 기본 API 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="378bc-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="378bc-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="378bc-113">Example 2</span></span>
```powershell
PS C:\> New-AzureRmMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount -KeyName Secondary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Secondary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="378bc-114">지정 된 Azure Maps 계정에 대 한 보조 API 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="378bc-114">Regenerates the Secondary API Key for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="378bc-115">변수</span><span class="sxs-lookup"><span data-stu-id="378bc-115">PARAMETERS</span></span>

### <span data-ttu-id="378bc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="378bc-116">-DefaultProfile</span></span>
<span data-ttu-id="378bc-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="378bc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378bc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="378bc-118">-InputObject</span></span>
<span data-ttu-id="378bc-119">AzureRmMapsAccount에서 파이프 맵 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="378bc-119">Maps Account piped from Get-AzureRmMapsAccount.</span></span>

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

### <span data-ttu-id="378bc-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="378bc-120">-KeyName</span></span>
<span data-ttu-id="378bc-121">지도 계정 키</span><span class="sxs-lookup"><span data-stu-id="378bc-121">Maps Account Key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="378bc-122">-이름</span><span class="sxs-lookup"><span data-stu-id="378bc-122">-Name</span></span>
<span data-ttu-id="378bc-123">계정 이름을 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="378bc-123">Maps Account Name.</span></span>

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

### <span data-ttu-id="378bc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="378bc-124">-ResourceGroupName</span></span>
<span data-ttu-id="378bc-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="378bc-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="378bc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="378bc-126">-ResourceId</span></span>
<span data-ttu-id="378bc-127">Maps 계정 ResourceId.</span><span class="sxs-lookup"><span data-stu-id="378bc-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="378bc-128">-확인</span><span class="sxs-lookup"><span data-stu-id="378bc-128">-Confirm</span></span>
<span data-ttu-id="378bc-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="378bc-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378bc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="378bc-130">-WhatIf</span></span>
<span data-ttu-id="378bc-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="378bc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="378bc-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="378bc-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378bc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="378bc-133">CommonParameters</span></span>
<span data-ttu-id="378bc-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="378bc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="378bc-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="378bc-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="378bc-136">입력</span><span class="sxs-lookup"><span data-stu-id="378bc-136">INPUTS</span></span>

### <span data-ttu-id="378bc-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="378bc-137">System.String</span></span>

### <span data-ttu-id="378bc-138">Microsoft Azure. \*. \*. \*.</span><span class="sxs-lookup"><span data-stu-id="378bc-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>
<span data-ttu-id="378bc-139">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="378bc-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="378bc-140">출력</span><span class="sxs-lookup"><span data-stu-id="378bc-140">OUTPUTS</span></span>

### <span data-ttu-id="378bc-141">Microsoft. s i m.-Saccount키</span><span class="sxs-lookup"><span data-stu-id="378bc-141">Microsoft.Azure.Management.Maps.Models.MapsAccountKeys</span></span>

## <span data-ttu-id="378bc-142">상속자</span><span class="sxs-lookup"><span data-stu-id="378bc-142">NOTES</span></span>

## <span data-ttu-id="378bc-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="378bc-143">RELATED LINKS</span></span>
