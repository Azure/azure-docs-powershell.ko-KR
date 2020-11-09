---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
ms.openlocfilehash: bdef7b776d8da82a357d535ff91298a2f49e9e4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304745"
---
# <span data-ttu-id="ab9d5-101">Remove-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="ab9d5-101">Remove-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="ab9d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab9d5-102">SYNOPSIS</span></span>
<span data-ttu-id="ab9d5-103">Windows 가상 데스크톱 등록 정보를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab9d5-103">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="ab9d5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ab9d5-104">SYNTAX</span></span>

```
Remove-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ab9d5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ab9d5-105">DESCRIPTION</span></span>
<span data-ttu-id="ab9d5-106">Windows 가상 데스크톱 등록 정보를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab9d5-106">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="ab9d5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ab9d5-107">EXAMPLES</span></span>

### <span data-ttu-id="ab9d5-108">예제 1: Windows 가상 데스크톱 등록 토큰 삭제</span><span class="sxs-lookup"><span data-stu-id="ab9d5-108">Example 1: Delete a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Remove-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName
```

<span data-ttu-id="ab9d5-109">이 명령은 호스트 풀에서 Windows 가상 데스크톱 등록 토큰을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab9d5-109">This command deletes a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="ab9d5-110">변수</span><span class="sxs-lookup"><span data-stu-id="ab9d5-110">PARAMETERS</span></span>

### <span data-ttu-id="ab9d5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab9d5-111">-DefaultProfile</span></span>
<span data-ttu-id="ab9d5-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ab9d5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab9d5-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="ab9d5-113">-HostPoolName</span></span>
<span data-ttu-id="ab9d5-114">호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="ab9d5-114">Host Pool Name</span></span>

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

### <span data-ttu-id="ab9d5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab9d5-115">-ResourceGroupName</span></span>
<span data-ttu-id="ab9d5-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ab9d5-116">Resource Group Name</span></span>

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

### <span data-ttu-id="ab9d5-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ab9d5-117">-SubscriptionId</span></span>
<span data-ttu-id="ab9d5-118">도움말 foo 1</span><span class="sxs-lookup"><span data-stu-id="ab9d5-118">help foo 1</span></span>

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

### <span data-ttu-id="ab9d5-119">-확인</span><span class="sxs-lookup"><span data-stu-id="ab9d5-119">-Confirm</span></span>
<span data-ttu-id="ab9d5-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab9d5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab9d5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab9d5-121">-WhatIf</span></span>
<span data-ttu-id="ab9d5-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ab9d5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab9d5-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab9d5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab9d5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab9d5-124">CommonParameters</span></span>
<span data-ttu-id="ab9d5-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab9d5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab9d5-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ab9d5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab9d5-127">입력</span><span class="sxs-lookup"><span data-stu-id="ab9d5-127">INPUTS</span></span>

## <span data-ttu-id="ab9d5-128">출력</span><span class="sxs-lookup"><span data-stu-id="ab9d5-128">OUTPUTS</span></span>

## <span data-ttu-id="ab9d5-129">상속자</span><span class="sxs-lookup"><span data-stu-id="ab9d5-129">NOTES</span></span>

<span data-ttu-id="ab9d5-130">별칭과</span><span class="sxs-lookup"><span data-stu-id="ab9d5-130">ALIASES</span></span>

## <span data-ttu-id="ab9d5-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab9d5-131">RELATED LINKS</span></span>

