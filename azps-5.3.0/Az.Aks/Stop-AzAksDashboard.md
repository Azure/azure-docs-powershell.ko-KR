---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 275a48f90e393f55fbd2d9df98471ce214b19a3f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492666"
---
# <span data-ttu-id="08e4d-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="08e4d-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="08e4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08e4d-102">SYNOPSIS</span></span>
<span data-ttu-id="08e4d-103">Start-AzKubernetesDashboard에서 만든 Kubectl SSH 터널을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="08e4d-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="08e4d-104">구문</span><span class="sxs-lookup"><span data-stu-id="08e4d-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08e4d-105">설명</span><span class="sxs-lookup"><span data-stu-id="08e4d-105">DESCRIPTION</span></span>
<span data-ttu-id="08e4d-106">Start-AzKubernetesDashboard에서 만든 Kubectl SSH 터널을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="08e4d-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="08e4d-107">예제</span><span class="sxs-lookup"><span data-stu-id="08e4d-107">EXAMPLES</span></span>

### <span data-ttu-id="08e4d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="08e4d-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="08e4d-109">Start-AzKubernetesDashboard를 실행하여 기존 SSH 터널 설정을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="08e4d-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="08e4d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08e4d-110">PARAMETERS</span></span>

### <span data-ttu-id="08e4d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08e4d-111">-DefaultProfile</span></span>
<span data-ttu-id="08e4d-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="08e4d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08e4d-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08e4d-113">-PassThru</span></span>
<span data-ttu-id="08e4d-114">SSH 터널이 닫혀 있는 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="08e4d-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="08e4d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08e4d-115">CommonParameters</span></span>
<span data-ttu-id="08e4d-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="08e4d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08e4d-117">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="08e4d-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08e4d-118">입력</span><span class="sxs-lookup"><span data-stu-id="08e4d-118">INPUTS</span></span>

### <span data-ttu-id="08e4d-119">없음</span><span class="sxs-lookup"><span data-stu-id="08e4d-119">None</span></span>

## <span data-ttu-id="08e4d-120">출력</span><span class="sxs-lookup"><span data-stu-id="08e4d-120">OUTPUTS</span></span>

### <span data-ttu-id="08e4d-121">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="08e4d-121">System.Boolean</span></span>

## <span data-ttu-id="08e4d-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="08e4d-122">NOTES</span></span>

## <span data-ttu-id="08e4d-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="08e4d-123">RELATED LINKS</span></span>
