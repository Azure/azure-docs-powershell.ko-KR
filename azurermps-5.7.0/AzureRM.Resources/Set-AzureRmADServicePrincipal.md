---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7B8C8239-16A3-4C47-9D6F-DE31885532F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADServicePrincipal.md
ms.openlocfilehash: 853404bce6d45f2824c574b249c434ccebc281ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534692"
---
# <span data-ttu-id="713f9-101">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="713f9-101">Set-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="713f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="713f9-102">SYNOPSIS</span></span>
<span data-ttu-id="713f9-103">기존 azure active directory 서비스 주체를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="713f9-103">Updates an existing azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="713f9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="713f9-104">SYNTAX</span></span>

### <span data-ttu-id="713f9-105">SpObjectIdWithDisplayNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="713f9-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Set-AzureRmADServicePrincipal -ObjectId <String> -DisplayName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="713f9-106">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="713f9-106">SPNWithDisplayNameParameterSet</span></span>
```
Set-AzureRmADServicePrincipal -ServicePrincipalName <String> -DisplayName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="713f9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="713f9-107">DESCRIPTION</span></span>
<span data-ttu-id="713f9-108">기존 azure active directory 서비스 주체를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="713f9-108">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="713f9-109">이 서비스 사용자와 연결 된 자격 증명을 업데이트 하려면 New-AzureRmADSpCredential cmdlet을 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="713f9-109">To update the credentials associated with this service principal, please use New-AzureRmADSpCredential cmdlet.</span></span> <span data-ttu-id="713f9-110">기본 응용 프로그램과 연결 된 속성을 업데이트 하려면 Set-AzureRmADApplication cmdlet을 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="713f9-110">To update the properties associated with the underlying application, please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="713f9-111">예제의</span><span class="sxs-lookup"><span data-stu-id="713f9-111">EXAMPLES</span></span>

### <span data-ttu-id="713f9-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="713f9-112">Example 1</span></span>
```
Set-AzureRmADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName "UpdatedNameForSp"
```

<span data-ttu-id="713f9-113">지정 된 개체 id로 서비스 주체의 표시 이름을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="713f9-113">Updates the display name for the service principal with specified object id.</span></span>

### <span data-ttu-id="713f9-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="713f9-114">Example 2</span></span>
```
Set-AzureRmADServicePrincipal -ServicePrincipalName "http://MyApp1" -DisplayName "UpdatedNameforSp"
```

<span data-ttu-id="713f9-115">지정 된 서비스 사용자 이름으로 서비스 사용자의 표시 이름을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="713f9-115">Updates the display name for the service principal with specified service principal name.</span></span>

## <span data-ttu-id="713f9-116">변수</span><span class="sxs-lookup"><span data-stu-id="713f9-116">PARAMETERS</span></span>

### <span data-ttu-id="713f9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="713f9-117">-DefaultProfile</span></span>
<span data-ttu-id="713f9-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="713f9-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="713f9-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="713f9-119">-DisplayName</span></span>
<span data-ttu-id="713f9-120">서비스 사용자의 새 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="713f9-120">New display name for the service principal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="713f9-121">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="713f9-121">-ObjectId</span></span>
<span data-ttu-id="713f9-122">업데이트할 서비스 주체의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="713f9-122">The object id of the service principal to update.</span></span>

```yaml
Type: String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="713f9-123">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="713f9-123">-ServicePrincipalName</span></span>
<span data-ttu-id="713f9-124">업데이트할 서비스 사용자의 SPN입니다.</span><span class="sxs-lookup"><span data-stu-id="713f9-124">The SPN of service principal to update.</span></span>

```yaml
Type: String
Parameter Sets: SPNWithDisplayNameParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="713f9-125">-확인</span><span class="sxs-lookup"><span data-stu-id="713f9-125">-Confirm</span></span>
<span data-ttu-id="713f9-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="713f9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="713f9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="713f9-127">-WhatIf</span></span>
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

### <span data-ttu-id="713f9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="713f9-128">CommonParameters</span></span>
<span data-ttu-id="713f9-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="713f9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="713f9-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="713f9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="713f9-131">입력</span><span class="sxs-lookup"><span data-stu-id="713f9-131">INPUTS</span></span>

### <span data-ttu-id="713f9-132">않아야</span><span class="sxs-lookup"><span data-stu-id="713f9-132">None</span></span>
<span data-ttu-id="713f9-133">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="713f9-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="713f9-134">출력</span><span class="sxs-lookup"><span data-stu-id="713f9-134">OUTPUTS</span></span>

## <span data-ttu-id="713f9-135">상속자</span><span class="sxs-lookup"><span data-stu-id="713f9-135">NOTES</span></span>

## <span data-ttu-id="713f9-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="713f9-136">RELATED LINKS</span></span>

[<span data-ttu-id="713f9-137">새로운 AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="713f9-137">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="713f9-138">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="713f9-138">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="713f9-139">제거-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="713f9-139">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="713f9-140">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="713f9-140">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="713f9-141">새로운 AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="713f9-141">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="713f9-142">제거-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="713f9-142">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

