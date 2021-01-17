---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 9e4ee275bf003dfa011eba4f00aad0029b5152de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334826"
---
# <span data-ttu-id="fb64a-101">Update-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="fb64a-101">Update-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="fb64a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb64a-102">SYNOPSIS</span></span>
<span data-ttu-id="fb64a-103">등록된 vCenter에 대한 검색 세부 정보를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="fb64a-103">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="fb64a-104">구문</span><span class="sxs-lookup"><span data-stu-id="fb64a-104">SYNTAX</span></span>

### <span data-ttu-id="fb64a-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="fb64a-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb64a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fb64a-106">ByResourceId</span></span>
```
Update-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb64a-107">설명</span><span class="sxs-lookup"><span data-stu-id="fb64a-107">DESCRIPTION</span></span>
<span data-ttu-id="fb64a-108">**Update-AzRecoveryServicesAsrvCenter** cmdlet은 등록된 vCenter에 대한 검색 세부 정보를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="fb64a-108">The **Update-AzRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="fb64a-109">예제</span><span class="sxs-lookup"><span data-stu-id="fb64a-109">EXAMPLES</span></span>

### <span data-ttu-id="fb64a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="fb64a-110">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="fb64a-111">등록된 vCenter에 대한 검색 세부 정보를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="fb64a-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="fb64a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb64a-112">PARAMETERS</span></span>

### <span data-ttu-id="fb64a-113">-Account</span><span class="sxs-lookup"><span data-stu-id="fb64a-113">-Account</span></span>
<span data-ttu-id="fb64a-114">vCenter 로그인 자격 증명 계정.</span><span class="sxs-lookup"><span data-stu-id="fb64a-114">vCenter login credentials account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb64a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb64a-115">-DefaultProfile</span></span>
<span data-ttu-id="fb64a-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fb64a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb64a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb64a-117">-InputObject</span></span>
<span data-ttu-id="fb64a-118">검색 세부 정보를 업데이트할 vCenter 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fb64a-118">The vCenter server object to update discovery details for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb64a-119">-Port</span><span class="sxs-lookup"><span data-stu-id="fb64a-119">-Port</span></span>
<span data-ttu-id="fb64a-120">검색에 사용할 vCenter 서버의 TCP 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="fb64a-120">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb64a-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb64a-121">-ResourceId</span></span>
<span data-ttu-id="fb64a-122">vCenter의 resourceId를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fb64a-122">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb64a-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb64a-123">-Confirm</span></span>
<span data-ttu-id="fb64a-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb64a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb64a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb64a-125">-WhatIf</span></span>
<span data-ttu-id="fb64a-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fb64a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb64a-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb64a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb64a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb64a-128">CommonParameters</span></span>
<span data-ttu-id="fb64a-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fb64a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb64a-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fb64a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb64a-131">입력</span><span class="sxs-lookup"><span data-stu-id="fb64a-131">INPUTS</span></span>

### <span data-ttu-id="fb64a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="fb64a-132">System.String</span></span>

### <span data-ttu-id="fb64a-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="fb64a-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="fb64a-134">출력</span><span class="sxs-lookup"><span data-stu-id="fb64a-134">OUTPUTS</span></span>

### <span data-ttu-id="fb64a-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="fb64a-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fb64a-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fb64a-136">NOTES</span></span>

## <span data-ttu-id="fb64a-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb64a-137">RELATED LINKS</span></span>
