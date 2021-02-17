---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
ms.openlocfilehash: bdef7b776d8da82a357d535ff91298a2f49e9e4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196433"
---
# <span data-ttu-id="55957-101">Remove-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="55957-101">Remove-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="55957-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55957-102">SYNOPSIS</span></span>
<span data-ttu-id="55957-103">Windows 가상 데스크톱 등록 정보를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="55957-103">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="55957-104">구문</span><span class="sxs-lookup"><span data-stu-id="55957-104">SYNTAX</span></span>

```
Remove-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="55957-105">설명</span><span class="sxs-lookup"><span data-stu-id="55957-105">DESCRIPTION</span></span>
<span data-ttu-id="55957-106">Windows 가상 데스크톱 등록 정보를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="55957-106">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="55957-107">예제</span><span class="sxs-lookup"><span data-stu-id="55957-107">EXAMPLES</span></span>

### <span data-ttu-id="55957-108">예제 1: Windows Virtual Desktop 등록 토큰 삭제</span><span class="sxs-lookup"><span data-stu-id="55957-108">Example 1: Delete a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Remove-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName
```

<span data-ttu-id="55957-109">이 명령은 호스트 풀에서 Windows Virtual Desktop 등록 토큰을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="55957-109">This command deletes a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="55957-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55957-110">PARAMETERS</span></span>

### <span data-ttu-id="55957-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55957-111">-DefaultProfile</span></span>
<span data-ttu-id="55957-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="55957-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55957-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="55957-113">-HostPoolName</span></span>
<span data-ttu-id="55957-114">호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="55957-114">Host Pool Name</span></span>

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

### <span data-ttu-id="55957-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55957-115">-ResourceGroupName</span></span>
<span data-ttu-id="55957-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="55957-116">Resource Group Name</span></span>

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

### <span data-ttu-id="55957-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="55957-117">-SubscriptionId</span></span>
<span data-ttu-id="55957-118">help foo 1</span><span class="sxs-lookup"><span data-stu-id="55957-118">help foo 1</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55957-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55957-119">-Confirm</span></span>
<span data-ttu-id="55957-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="55957-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55957-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55957-121">-WhatIf</span></span>
<span data-ttu-id="55957-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="55957-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55957-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="55957-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55957-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55957-124">CommonParameters</span></span>
<span data-ttu-id="55957-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="55957-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55957-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="55957-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55957-127">입력</span><span class="sxs-lookup"><span data-stu-id="55957-127">INPUTS</span></span>

## <span data-ttu-id="55957-128">출력</span><span class="sxs-lookup"><span data-stu-id="55957-128">OUTPUTS</span></span>

## <span data-ttu-id="55957-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="55957-129">NOTES</span></span>

<span data-ttu-id="55957-130">별칭</span><span class="sxs-lookup"><span data-stu-id="55957-130">ALIASES</span></span>

## <span data-ttu-id="55957-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="55957-131">RELATED LINKS</span></span>

