---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
ms.openlocfilehash: b24fe9e6587fe50a41d601c70c2687891bea2f16
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305219"
---
# <span data-ttu-id="2b5b4-101">New-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="2b5b4-101">New-AzDataShareAccount</span></span>

## <span data-ttu-id="2b5b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b5b4-102">SYNOPSIS</span></span>
<span data-ttu-id="2b5b4-103">새 데이터 공유 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="2b5b4-103">Creates new data share account</span></span>

## <span data-ttu-id="2b5b4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2b5b4-104">SYNTAX</span></span>

```
New-AzDataShareAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b5b4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2b5b4-105">DESCRIPTION</span></span>
<span data-ttu-id="2b5b4-106">**AzDataShareAccount** cmdlet은 지정 된 Azure 리소스 그룹에 datashare account를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2b5b4-106">**New-AzDataShareAccount** cmdlet creates a datashare account in the specified Azure resource group.</span></span>

## <span data-ttu-id="2b5b4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2b5b4-107">EXAMPLES</span></span>

### <span data-ttu-id="2b5b4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2b5b4-108">Example 1</span></span>
```
PS C:\> New-AzDataShareAccount -ResourceGroupName "ADS" -Name "WikiADS" -Location "WestUS"
DataShareAccountName   : WikiADS
ResourceGroupName : ADS
Location          : WestUS
ProvisioningState : Succeeded
Tags              : {}
Identity          : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type              : Microsoft.DataShare/accounts
Id                : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
```

<span data-ttu-id="2b5b4-109">"WikiADS" 라는 계정을 "ADS" 리소스 그룹에 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2b5b4-109">Creates an account named "WikiADS" in resource group "ADS"</span></span>

## <span data-ttu-id="2b5b4-110">변수</span><span class="sxs-lookup"><span data-stu-id="2b5b4-110">PARAMETERS</span></span>

### <span data-ttu-id="2b5b4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b5b4-111">-AsJob</span></span>
<span data-ttu-id="2b5b4-112">{{AsJob 입력 기술}}</span><span class="sxs-lookup"><span data-stu-id="2b5b4-112">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="2b5b4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b5b4-113">-DefaultProfile</span></span>
<span data-ttu-id="2b5b4-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2b5b4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b5b4-115">-위치</span><span class="sxs-lookup"><span data-stu-id="2b5b4-115">-Location</span></span>
<span data-ttu-id="2b5b4-116">데이터 공유 계정을 만들 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="2b5b4-116">The location in which to create the data share account.</span></span>

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

### <span data-ttu-id="2b5b4-117">-이름</span><span class="sxs-lookup"><span data-stu-id="2b5b4-117">-Name</span></span>
<span data-ttu-id="2b5b4-118">Azure data share 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b5b4-118">Azure data share account name.</span></span>

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

### <span data-ttu-id="2b5b4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b5b4-119">-ResourceGroupName</span></span>
<span data-ttu-id="2b5b4-120">Azure data share 계정에 대 한 리소스 그룹 이름이에 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b5b4-120">The resource group name of the azure data share account will be created in.</span></span>

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

### <span data-ttu-id="2b5b4-121">태그</span><span class="sxs-lookup"><span data-stu-id="2b5b4-121">-Tag</span></span>
<span data-ttu-id="2b5b4-122">Azure data share 계정과 연결할 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="2b5b4-122">The tags to associate with the azure data share account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b5b4-123">-확인</span><span class="sxs-lookup"><span data-stu-id="2b5b4-123">-Confirm</span></span>
<span data-ttu-id="2b5b4-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b5b4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b5b4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b5b4-125">-WhatIf</span></span>
<span data-ttu-id="2b5b4-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2b5b4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b5b4-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2b5b4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b5b4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b5b4-128">CommonParameters</span></span>
<span data-ttu-id="2b5b4-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b5b4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b5b4-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2b5b4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b5b4-131">입력</span><span class="sxs-lookup"><span data-stu-id="2b5b4-131">INPUTS</span></span>

### <span data-ttu-id="2b5b4-132">않아야</span><span class="sxs-lookup"><span data-stu-id="2b5b4-132">None</span></span>

## <span data-ttu-id="2b5b4-133">출력</span><span class="sxs-lookup"><span data-stu-id="2b5b4-133">OUTPUTS</span></span>

### <span data-ttu-id="2b5b4-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="2b5b4-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="2b5b4-135">상속자</span><span class="sxs-lookup"><span data-stu-id="2b5b4-135">NOTES</span></span>

## <span data-ttu-id="2b5b4-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b5b4-136">RELATED LINKS</span></span>
