---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
ms.openlocfilehash: 265f917068237fee13f77eb8c87e0adf8cd12f08
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186105"
---
# <span data-ttu-id="1053e-101">New-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="1053e-101">New-AzDataShare</span></span>

## <span data-ttu-id="1053e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1053e-102">SYNOPSIS</span></span>
<span data-ttu-id="1053e-103">Azure 데이터 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1053e-103">Creates a azure data share.</span></span>

## <span data-ttu-id="1053e-104">구문</span><span class="sxs-lookup"><span data-stu-id="1053e-104">SYNTAX</span></span>

```
New-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1053e-105">설명</span><span class="sxs-lookup"><span data-stu-id="1053e-105">DESCRIPTION</span></span>
<span data-ttu-id="1053e-106">**New-AzDataShare** cmdlet은 리소스 그룹 이름, 계정 이름, 공유 이름 및 공유 종류를 제공하여 지정된 Azure 데이터 공유 계정 내에서 데이터 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1053e-106">The **New-AzDataShare** cmdlet creates a data share within a specified azure data share account by providing the resource group name, account name, share name and share kind.</span></span> <span data-ttu-id="1053e-107">설명 및 사용 약관은 데이터 공유를 만드는 동안 설정할 수 있는 선택적 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="1053e-107">Description and terms of use are optional parameters that can be set while creating the data share.</span></span>

## <span data-ttu-id="1053e-108">예제</span><span class="sxs-lookup"><span data-stu-id="1053e-108">EXAMPLES</span></span>

### <span data-ttu-id="1053e-109">예제 1: 데이터 공유 만들기</span><span class="sxs-lookup"><span data-stu-id="1053e-109">Example 1 : Create a data share</span></span>
```
PS C:\>New-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare" -ShareKind "CopyBased" -Description "Example of description" -TermsOfUse "This should not be shared"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Example of description  
ProvisioningState   : Succeeded
Terms               : This should not be shared
```

<span data-ttu-id="1053e-110">이 명령은 설명 및 사용 약관이 있는 리소스 그룹 ADS 아래에 데이터 공유 계정 WikiAdsAccount에 CopyBased 종류의 AdsShare라는 데이터 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1053e-110">This command creates a data share named AdsShare of kind CopyBased in data share account WikiAdsAccount under resource group ADS with description and terms of use.</span></span>

## <span data-ttu-id="1053e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1053e-111">PARAMETERS</span></span>

### <span data-ttu-id="1053e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1053e-112">-AccountName</span></span>
<span data-ttu-id="1053e-113">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="1053e-113">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1053e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1053e-114">-DefaultProfile</span></span>
<span data-ttu-id="1053e-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1053e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1053e-116">-Description</span><span class="sxs-lookup"><span data-stu-id="1053e-116">-Description</span></span>
<span data-ttu-id="1053e-117">Azure 데이터 공유에 대한 설명</span><span class="sxs-lookup"><span data-stu-id="1053e-117">Description of azure data share</span></span>

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

### <span data-ttu-id="1053e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1053e-118">-Name</span></span>
<span data-ttu-id="1053e-119">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="1053e-119">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1053e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1053e-120">-ResourceGroupName</span></span>
<span data-ttu-id="1053e-121">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="1053e-121">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1053e-122">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="1053e-122">-TermsOfUse</span></span>
<span data-ttu-id="1053e-123">Azure 데이터 공유에 대한 사용 약관</span><span class="sxs-lookup"><span data-stu-id="1053e-123">Terms of use for azure data share</span></span>

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

### <span data-ttu-id="1053e-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1053e-124">-Confirm</span></span>
<span data-ttu-id="1053e-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1053e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1053e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1053e-126">-WhatIf</span></span>
<span data-ttu-id="1053e-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1053e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1053e-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1053e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1053e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1053e-129">CommonParameters</span></span>
<span data-ttu-id="1053e-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1053e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1053e-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1053e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1053e-132">입력</span><span class="sxs-lookup"><span data-stu-id="1053e-132">INPUTS</span></span>

### <span data-ttu-id="1053e-133">없음</span><span class="sxs-lookup"><span data-stu-id="1053e-133">None</span></span>

## <span data-ttu-id="1053e-134">출력</span><span class="sxs-lookup"><span data-stu-id="1053e-134">OUTPUTS</span></span>

### <span data-ttu-id="1053e-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="1053e-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="1053e-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1053e-136">NOTES</span></span>

## <span data-ttu-id="1053e-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1053e-137">RELATED LINKS</span></span>
