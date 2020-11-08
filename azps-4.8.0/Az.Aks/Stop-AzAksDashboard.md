---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 275a48f90e393f55fbd2d9df98471ce214b19a3f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204143"
---
# <span data-ttu-id="7efcd-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="7efcd-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="7efcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7efcd-102">SYNOPSIS</span></span>
<span data-ttu-id="7efcd-103">시작-AzKubernetesDashboard에서 만든 Kubectl SSH 터널을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7efcd-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="7efcd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7efcd-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7efcd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7efcd-105">DESCRIPTION</span></span>
<span data-ttu-id="7efcd-106">시작-AzKubernetesDashboard에서 만든 Kubectl SSH 터널을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7efcd-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="7efcd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7efcd-107">EXAMPLES</span></span>

### <span data-ttu-id="7efcd-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7efcd-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="7efcd-109">시작-AzKubernetesDashboard를 실행 하 여 기존 SSH 터널 설정을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7efcd-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="7efcd-110">변수</span><span class="sxs-lookup"><span data-stu-id="7efcd-110">PARAMETERS</span></span>

### <span data-ttu-id="7efcd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7efcd-111">-DefaultProfile</span></span>
<span data-ttu-id="7efcd-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7efcd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7efcd-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7efcd-113">-PassThru</span></span>
<span data-ttu-id="7efcd-114">SSH 터널이 닫혀 있으면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7efcd-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="7efcd-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7efcd-115">CommonParameters</span></span>
<span data-ttu-id="7efcd-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7efcd-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7efcd-117">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7efcd-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7efcd-118">입력</span><span class="sxs-lookup"><span data-stu-id="7efcd-118">INPUTS</span></span>

### <span data-ttu-id="7efcd-119">않아야</span><span class="sxs-lookup"><span data-stu-id="7efcd-119">None</span></span>

## <span data-ttu-id="7efcd-120">출력</span><span class="sxs-lookup"><span data-stu-id="7efcd-120">OUTPUTS</span></span>

### <span data-ttu-id="7efcd-121">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="7efcd-121">System.Boolean</span></span>

## <span data-ttu-id="7efcd-122">상속자</span><span class="sxs-lookup"><span data-stu-id="7efcd-122">NOTES</span></span>

## <span data-ttu-id="7efcd-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7efcd-123">RELATED LINKS</span></span>
