---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/set-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
ms.openlocfilehash: 69d44ea88b34aba027933cb3015a203bf06070fd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305114"
---
# <span data-ttu-id="ed153-101">Set-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="ed153-101">Set-AzDataShare</span></span>

## <span data-ttu-id="ed153-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed153-102">SYNOPSIS</span></span>
<span data-ttu-id="ed153-103">기존 데이터 공유 업데이트</span><span class="sxs-lookup"><span data-stu-id="ed153-103">Updates an existing data share</span></span>

## <span data-ttu-id="ed153-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ed153-104">SYNTAX</span></span>

### <span data-ttu-id="ed153-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ed153-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed153-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed153-106">ByResourceIdParameterSet</span></span>
```
Set-AzDataShare -ResourceId <String> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed153-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed153-107">ByObjectParameterSet</span></span>
```
Set-AzDataShare -InputObject <PSDataShare> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed153-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ed153-108">DESCRIPTION</span></span>
<span data-ttu-id="ed153-109">**AzDataShare** cmdlet은 지정 된 azure data 공유 계정 내에 있는 데이터 공유를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed153-109">The **Set-AzDataShare** cmdlet updates a data share that exists within a specified azure data share account.</span></span>

## <span data-ttu-id="ed153-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ed153-110">EXAMPLES</span></span>

### <span data-ttu-id="ed153-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ed153-111">Example 1</span></span>
```
PS C:\> Set-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare" -Description "Updated description" -TermsOfUse "Updated terms"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Updated description
ProvisioningState   : Succeeded
Terms               : Updated terms
```

<span data-ttu-id="ed153-112">이 명령은 AdsShare 라는 기존 데이터 공유를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed153-112">This command updates an existing data share named AdsShare</span></span>

## <span data-ttu-id="ed153-113">변수</span><span class="sxs-lookup"><span data-stu-id="ed153-113">PARAMETERS</span></span>

### <span data-ttu-id="ed153-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ed153-114">-AccountName</span></span>
<span data-ttu-id="ed153-115">Azure data share 계정 이름</span><span class="sxs-lookup"><span data-stu-id="ed153-115">Azure data share account name</span></span>

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

### <span data-ttu-id="ed153-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed153-116">-DefaultProfile</span></span>
<span data-ttu-id="ed153-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ed153-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed153-118">-설명</span><span class="sxs-lookup"><span data-stu-id="ed153-118">-Description</span></span>
<span data-ttu-id="ed153-119">데이터 공유에 대 한 설명</span><span class="sxs-lookup"><span data-stu-id="ed153-119">Description of Data Share</span></span>

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

### <span data-ttu-id="ed153-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed153-120">-InputObject</span></span>
<span data-ttu-id="ed153-121">Azure data share 개체</span><span class="sxs-lookup"><span data-stu-id="ed153-121">Azure data share object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed153-122">-이름</span><span class="sxs-lookup"><span data-stu-id="ed153-122">-Name</span></span>
<span data-ttu-id="ed153-123">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="ed153-123">Azure data share name</span></span>

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

### <span data-ttu-id="ed153-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed153-124">-ResourceGroupName</span></span>
<span data-ttu-id="ed153-125">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ed153-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="ed153-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed153-126">-ResourceId</span></span>
<span data-ttu-id="ed153-127">Azure data share의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="ed153-127">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="ed153-128">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="ed153-128">-TermsOfUse</span></span>
<span data-ttu-id="ed153-129">데이터 공유 사용 약관</span><span class="sxs-lookup"><span data-stu-id="ed153-129">Terms of Use for Data Share</span></span>

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

### <span data-ttu-id="ed153-130">-확인</span><span class="sxs-lookup"><span data-stu-id="ed153-130">-Confirm</span></span>
<span data-ttu-id="ed153-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed153-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed153-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed153-132">-WhatIf</span></span>
<span data-ttu-id="ed153-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ed153-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed153-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed153-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed153-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed153-135">CommonParameters</span></span>
<span data-ttu-id="ed153-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed153-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed153-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ed153-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed153-138">입력</span><span class="sxs-lookup"><span data-stu-id="ed153-138">INPUTS</span></span>

### <span data-ttu-id="ed153-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ed153-139">System.String</span></span>

### <span data-ttu-id="ed153-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="ed153-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="ed153-141">출력</span><span class="sxs-lookup"><span data-stu-id="ed153-141">OUTPUTS</span></span>

### <span data-ttu-id="ed153-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="ed153-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="ed153-143">상속자</span><span class="sxs-lookup"><span data-stu-id="ed153-143">NOTES</span></span>

## <span data-ttu-id="ed153-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed153-144">RELATED LINKS</span></span>
