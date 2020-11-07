---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 4d4e2a86bfa2974cabcc4208f7a314019f5804e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689204"
---
# <span data-ttu-id="d7f8a-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="d7f8a-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="d7f8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7f8a-102">SYNOPSIS</span></span>
<span data-ttu-id="d7f8a-103">시작-AzKubernetesDashboard에서 만든 Kubectl SSH 터널을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f8a-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="d7f8a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d7f8a-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7f8a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d7f8a-105">DESCRIPTION</span></span>
<span data-ttu-id="d7f8a-106">시작-AzKubernetesDashboard에서 만든 Kubectl SSH 터널을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f8a-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="d7f8a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d7f8a-107">EXAMPLES</span></span>

### <span data-ttu-id="d7f8a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d7f8a-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="d7f8a-109">시작-AzKubernetesDashboard를 실행 하 여 기존 SSH 터널 설정을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f8a-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="d7f8a-110">변수</span><span class="sxs-lookup"><span data-stu-id="d7f8a-110">PARAMETERS</span></span>

### <span data-ttu-id="d7f8a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7f8a-111">-DefaultProfile</span></span>
<span data-ttu-id="d7f8a-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d7f8a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7f8a-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7f8a-113">-PassThru</span></span>
<span data-ttu-id="d7f8a-114">SSH 터널이 닫혀 있으면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f8a-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="d7f8a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7f8a-115">CommonParameters</span></span>
<span data-ttu-id="d7f8a-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f8a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7f8a-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7f8a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7f8a-118">입력</span><span class="sxs-lookup"><span data-stu-id="d7f8a-118">INPUTS</span></span>

### <span data-ttu-id="d7f8a-119">않아야</span><span class="sxs-lookup"><span data-stu-id="d7f8a-119">None</span></span>

## <span data-ttu-id="d7f8a-120">출력</span><span class="sxs-lookup"><span data-stu-id="d7f8a-120">OUTPUTS</span></span>

### <span data-ttu-id="d7f8a-121">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="d7f8a-121">System.Boolean</span></span>

## <span data-ttu-id="d7f8a-122">상속자</span><span class="sxs-lookup"><span data-stu-id="d7f8a-122">NOTES</span></span>

## <span data-ttu-id="d7f8a-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7f8a-123">RELATED LINKS</span></span>
