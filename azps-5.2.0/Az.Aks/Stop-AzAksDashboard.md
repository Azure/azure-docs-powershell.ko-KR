---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 275a48f90e393f55fbd2d9df98471ce214b19a3f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335774"
---
# <span data-ttu-id="d8c36-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="d8c36-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="d8c36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8c36-102">SYNOPSIS</span></span>
<span data-ttu-id="d8c36-103">Start-AzKubernetesDashboard에서 만든 Kubectl SSH 터널을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="d8c36-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="d8c36-104">구문</span><span class="sxs-lookup"><span data-stu-id="d8c36-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8c36-105">설명</span><span class="sxs-lookup"><span data-stu-id="d8c36-105">DESCRIPTION</span></span>
<span data-ttu-id="d8c36-106">Start-AzKubernetesDashboard에서 만든 Kubectl SSH 터널을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="d8c36-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="d8c36-107">예제</span><span class="sxs-lookup"><span data-stu-id="d8c36-107">EXAMPLES</span></span>

### <span data-ttu-id="d8c36-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d8c36-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="d8c36-109">Start-AzKubernetesDashboard를 실행하여 기존 SSH 터널 설정을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="d8c36-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="d8c36-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8c36-110">PARAMETERS</span></span>

### <span data-ttu-id="d8c36-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8c36-111">-DefaultProfile</span></span>
<span data-ttu-id="d8c36-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c36-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8c36-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8c36-113">-PassThru</span></span>
<span data-ttu-id="d8c36-114">SSH 터널이 닫혀 있는 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d8c36-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="d8c36-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8c36-115">CommonParameters</span></span>
<span data-ttu-id="d8c36-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d8c36-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8c36-117">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d8c36-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8c36-118">입력</span><span class="sxs-lookup"><span data-stu-id="d8c36-118">INPUTS</span></span>

### <span data-ttu-id="d8c36-119">없음</span><span class="sxs-lookup"><span data-stu-id="d8c36-119">None</span></span>

## <span data-ttu-id="d8c36-120">출력</span><span class="sxs-lookup"><span data-stu-id="d8c36-120">OUTPUTS</span></span>

### <span data-ttu-id="d8c36-121">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d8c36-121">System.Boolean</span></span>

## <span data-ttu-id="d8c36-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d8c36-122">NOTES</span></span>

## <span data-ttu-id="d8c36-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8c36-123">RELATED LINKS</span></span>
