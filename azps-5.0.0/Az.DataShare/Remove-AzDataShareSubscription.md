---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: eb2b7f1e22ff3d2fccdff0d84a77f5c68ca8e70d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305138"
---
# <span data-ttu-id="46105-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="46105-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="46105-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46105-102">SYNOPSIS</span></span>
<span data-ttu-id="46105-103">공유 구독 제거</span><span class="sxs-lookup"><span data-stu-id="46105-103">removes a share subscription</span></span>

## <span data-ttu-id="46105-104">구문과</span><span class="sxs-lookup"><span data-stu-id="46105-104">SYNTAX</span></span>

### <span data-ttu-id="46105-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="46105-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46105-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="46105-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46105-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46105-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46105-108">설명은</span><span class="sxs-lookup"><span data-stu-id="46105-108">DESCRIPTION</span></span>
<span data-ttu-id="46105-109">AzDataShareSubscription cmdlet이 공유 구독을 제거 **함**</span><span class="sxs-lookup"><span data-stu-id="46105-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="46105-110">예제의</span><span class="sxs-lookup"><span data-stu-id="46105-110">EXAMPLES</span></span>

### <span data-ttu-id="46105-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="46105-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="46105-112">이 명령은 AdsShareSubscription에서 sharesubscription 이라는 이름을 account WikiAds에서 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="46105-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="46105-113">변수</span><span class="sxs-lookup"><span data-stu-id="46105-113">PARAMETERS</span></span>

### <span data-ttu-id="46105-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="46105-114">-AccountName</span></span>
<span data-ttu-id="46105-115">Azure data share 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="46105-115">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46105-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46105-116">-AsJob</span></span>
<span data-ttu-id="46105-117">{{AsJob 입력 기술}}</span><span class="sxs-lookup"><span data-stu-id="46105-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="46105-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46105-118">-DefaultProfile</span></span>
<span data-ttu-id="46105-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="46105-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46105-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46105-120">-InputObject</span></span>
<span data-ttu-id="46105-121">Azure data share 구독 개체</span><span class="sxs-lookup"><span data-stu-id="46105-121">Azure data share subscription object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46105-122">-이름</span><span class="sxs-lookup"><span data-stu-id="46105-122">-Name</span></span>
<span data-ttu-id="46105-123">Azure data share 구독 이름</span><span class="sxs-lookup"><span data-stu-id="46105-123">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46105-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46105-124">-PassThru</span></span>
<span data-ttu-id="46105-125">Object (지정 된 경우)를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="46105-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="46105-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46105-126">-ResourceGroupName</span></span>
<span data-ttu-id="46105-127">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="46105-127">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46105-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46105-128">-ResourceId</span></span>
<span data-ttu-id="46105-129">Azure data share 구독의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="46105-129">The resource id of the azure data share subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46105-130">-확인</span><span class="sxs-lookup"><span data-stu-id="46105-130">-Confirm</span></span>
<span data-ttu-id="46105-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="46105-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46105-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46105-132">-WhatIf</span></span>
<span data-ttu-id="46105-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="46105-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46105-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46105-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46105-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46105-135">CommonParameters</span></span>
<span data-ttu-id="46105-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="46105-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46105-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="46105-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46105-138">입력</span><span class="sxs-lookup"><span data-stu-id="46105-138">INPUTS</span></span>

### <span data-ttu-id="46105-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="46105-139">System.String</span></span>

### <span data-ttu-id="46105-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="46105-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="46105-141">출력</span><span class="sxs-lookup"><span data-stu-id="46105-141">OUTPUTS</span></span>

### <span data-ttu-id="46105-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="46105-142">System.Boolean</span></span>

## <span data-ttu-id="46105-143">상속자</span><span class="sxs-lookup"><span data-stu-id="46105-143">NOTES</span></span>

## <span data-ttu-id="46105-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46105-144">RELATED LINKS</span></span>
