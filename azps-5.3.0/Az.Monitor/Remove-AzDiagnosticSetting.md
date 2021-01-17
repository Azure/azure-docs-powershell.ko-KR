---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
ms.openlocfilehash: f165396d5b3af823d91e7c06d2f1cb93eb2eaafd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385680"
---
# <span data-ttu-id="615e4-101">Remove-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="615e4-101">Remove-AzDiagnosticSetting</span></span>

## <span data-ttu-id="615e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="615e4-102">SYNOPSIS</span></span>
<span data-ttu-id="615e4-103">리소스에 대한 진단 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="615e4-103">Remove a diagnostic setting for the a resource.</span></span>

## <span data-ttu-id="615e4-104">구문</span><span class="sxs-lookup"><span data-stu-id="615e4-104">SYNTAX</span></span>

```
Remove-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="615e4-105">설명</span><span class="sxs-lookup"><span data-stu-id="615e4-105">DESCRIPTION</span></span>
<span data-ttu-id="615e4-106">**Remove-AzDiagnosticSetting** cmdlet은 특정 리소스에 대한 진단 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="615e4-106">The **Remove-AzDiagnosticSetting** cmdlet removes the diagnostic setting for the particular resource.</span></span>
<span data-ttu-id="615e4-107">이 cmdlet은 ShouldProcess 패턴을 구현합니다. 즉, 리소스를 실제로 만들거나 수정하거나 제거하기 전에 사용자로부터 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="615e4-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="615e4-108">예제</span><span class="sxs-lookup"><span data-stu-id="615e4-108">EXAMPLES</span></span>

### <span data-ttu-id="615e4-109">예제 1: 리소스에 대한 기본 진단 설정(서비스) 제거</span><span class="sxs-lookup"><span data-stu-id="615e4-109">Example 1: Remove the default diagnostic setting (service) for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01"
```

<span data-ttu-id="615e4-110">이 명령은 Resource01이라는 리소스에 대한 기본 진단 설정(서비스)을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="615e4-110">This command removes the default diagnostic setting (service) for the resource called Resource01.</span></span>

### <span data-ttu-id="615e4-111">예제 2: 리소스에 대해 지정한 이름으로 식별된 기본 진단 설정 제거</span><span class="sxs-lookup"><span data-stu-id="615e4-111">Example 2: Remove the default diagnostic setting identified by the given name for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01" -Name myDiagSetting
```

<span data-ttu-id="615e4-112">이 명령은 Resource01이라는 리소스에 대한 myDiagSetting이라는 진단 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="615e4-112">This command removes the diagnostic setting called myDiagSetting for the resource called Resource01.</span></span>

## <span data-ttu-id="615e4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="615e4-113">PARAMETERS</span></span>

### <span data-ttu-id="615e4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="615e4-114">-DefaultProfile</span></span>
<span data-ttu-id="615e4-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="615e4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="615e4-116">-Name</span><span class="sxs-lookup"><span data-stu-id="615e4-116">-Name</span></span>
<span data-ttu-id="615e4-117">진단 설정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="615e4-117">The name of the diagnostic setting.</span></span> <span data-ttu-id="615e4-118">호출 기본값을 이전 API와 동일하게 지정하지 않은 경우 이 cmdlet은 메트릭/로그에 대한 모든 범주만 비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="615e4-118">If not given the call default to "service" as it was in the previous API and this cmdlet will only disable all categories for metrics/logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="615e4-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="615e4-119">-ResourceId</span></span>
<span data-ttu-id="615e4-120">리소스의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="615e4-120">Specifies the ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="615e4-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="615e4-121">-Confirm</span></span>
<span data-ttu-id="615e4-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="615e4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="615e4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="615e4-123">-WhatIf</span></span>
<span data-ttu-id="615e4-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="615e4-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="615e4-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="615e4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="615e4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="615e4-126">CommonParameters</span></span>
<span data-ttu-id="615e4-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="615e4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="615e4-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="615e4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="615e4-129">입력</span><span class="sxs-lookup"><span data-stu-id="615e4-129">INPUTS</span></span>

### <span data-ttu-id="615e4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="615e4-130">System.String</span></span>

## <span data-ttu-id="615e4-131">출력</span><span class="sxs-lookup"><span data-stu-id="615e4-131">OUTPUTS</span></span>

### <span data-ttu-id="615e4-132">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="615e4-132">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="615e4-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="615e4-133">NOTES</span></span>

## <span data-ttu-id="615e4-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="615e4-134">RELATED LINKS</span></span>

<span data-ttu-id="615e4-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="615e4-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span></span>
