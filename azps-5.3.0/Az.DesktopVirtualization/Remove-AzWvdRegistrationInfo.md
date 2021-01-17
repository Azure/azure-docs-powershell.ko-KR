---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
ms.openlocfilehash: bdef7b776d8da82a357d535ff91298a2f49e9e4c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492053"
---
# <span data-ttu-id="54bf6-101">Remove-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="54bf6-101">Remove-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="54bf6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54bf6-102">SYNOPSIS</span></span>
<span data-ttu-id="54bf6-103">Windows 가상 데스크톱 등록 정보를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="54bf6-103">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="54bf6-104">구문</span><span class="sxs-lookup"><span data-stu-id="54bf6-104">SYNTAX</span></span>

```
Remove-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="54bf6-105">설명</span><span class="sxs-lookup"><span data-stu-id="54bf6-105">DESCRIPTION</span></span>
<span data-ttu-id="54bf6-106">Windows 가상 데스크톱 등록 정보를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="54bf6-106">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="54bf6-107">예제</span><span class="sxs-lookup"><span data-stu-id="54bf6-107">EXAMPLES</span></span>

### <span data-ttu-id="54bf6-108">예제 1: Windows Virtual Desktop 등록 토큰 삭제</span><span class="sxs-lookup"><span data-stu-id="54bf6-108">Example 1: Delete a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Remove-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName
```

<span data-ttu-id="54bf6-109">이 명령은 호스트 풀에서 Windows Virtual Desktop 등록 토큰을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="54bf6-109">This command deletes a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="54bf6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54bf6-110">PARAMETERS</span></span>

### <span data-ttu-id="54bf6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54bf6-111">-DefaultProfile</span></span>
<span data-ttu-id="54bf6-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="54bf6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54bf6-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="54bf6-113">-HostPoolName</span></span>
<span data-ttu-id="54bf6-114">호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="54bf6-114">Host Pool Name</span></span>

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

### <span data-ttu-id="54bf6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54bf6-115">-ResourceGroupName</span></span>
<span data-ttu-id="54bf6-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="54bf6-116">Resource Group Name</span></span>

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

### <span data-ttu-id="54bf6-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="54bf6-117">-SubscriptionId</span></span>
<span data-ttu-id="54bf6-118">도움말 foo 1</span><span class="sxs-lookup"><span data-stu-id="54bf6-118">help foo 1</span></span>

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

### <span data-ttu-id="54bf6-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54bf6-119">-Confirm</span></span>
<span data-ttu-id="54bf6-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="54bf6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54bf6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54bf6-121">-WhatIf</span></span>
<span data-ttu-id="54bf6-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="54bf6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54bf6-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="54bf6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54bf6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54bf6-124">CommonParameters</span></span>
<span data-ttu-id="54bf6-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="54bf6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54bf6-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="54bf6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54bf6-127">입력</span><span class="sxs-lookup"><span data-stu-id="54bf6-127">INPUTS</span></span>

## <span data-ttu-id="54bf6-128">출력</span><span class="sxs-lookup"><span data-stu-id="54bf6-128">OUTPUTS</span></span>

## <span data-ttu-id="54bf6-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="54bf6-129">NOTES</span></span>

<span data-ttu-id="54bf6-130">별칭</span><span class="sxs-lookup"><span data-stu-id="54bf6-130">ALIASES</span></span>

## <span data-ttu-id="54bf6-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54bf6-131">RELATED LINKS</span></span>

