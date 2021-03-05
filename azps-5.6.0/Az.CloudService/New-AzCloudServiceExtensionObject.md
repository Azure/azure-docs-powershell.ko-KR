---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceExtensionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceExtensionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceExtensionObject.md
ms.openlocfilehash: d37a717ba87771310de4f1944e3865712e00554e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986188"
---
# <span data-ttu-id="954d3-101">New-AzCloudServiceExtensionObject</span><span class="sxs-lookup"><span data-stu-id="954d3-101">New-AzCloudServiceExtensionObject</span></span>

## <span data-ttu-id="954d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="954d3-102">SYNOPSIS</span></span>
<span data-ttu-id="954d3-103">확장용 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="954d3-103">Create a in-memory object for Extension</span></span>

## <span data-ttu-id="954d3-104">구문</span><span class="sxs-lookup"><span data-stu-id="954d3-104">SYNTAX</span></span>

```
New-AzCloudServiceExtensionObject [-AutoUpgradeMinorVersion <Boolean>] [-Name <String>]
 [-ProtectedSetting <String>] [-Publisher <String>] [-RolesAppliedTo <String[]>] [-Setting <String>]
 [-Type <String>] [-TypeHandlerVersion <String>] [<CommonParameters>]
```

## <span data-ttu-id="954d3-105">설명</span><span class="sxs-lookup"><span data-stu-id="954d3-105">DESCRIPTION</span></span>
<span data-ttu-id="954d3-106">확장용 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="954d3-106">Create a in-memory object for Extension</span></span>

## <span data-ttu-id="954d3-107">예제</span><span class="sxs-lookup"><span data-stu-id="954d3-107">EXAMPLES</span></span>

### <span data-ttu-id="954d3-108">예제 1: Geneva 확장 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="954d3-108">Example 1: Create Geneva extension object</span></span>
```powershell
PS C:\> $extension = New-AzCloudServiceExtensionObject -Name "GenevaExtension" -Publisher "Microsoft.Azure.Geneva" -Type "GenevaMonitoringPaaS" -TypeHandlerVersion "2.14.0.2"
```

<span data-ttu-id="954d3-109">이 명령은 클라우드 서비스를 만들거나 업데이트하는 데 사용되는 Geneva 확장 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="954d3-109">This command creates Geneva extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="954d3-110">자세한 내용은 New-AzCloudService를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="954d3-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="954d3-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="954d3-111">PARAMETERS</span></span>

### <span data-ttu-id="954d3-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="954d3-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="954d3-113">CRP가 사용할 수 있게 될 때 TypeHandlerVersion을 더 높은 부 버전으로 자동으로 업그레이드할 수 있는지 여부를 명시적으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="954d3-113">Explicitly specify whether CRP can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="954d3-114">-Name</span><span class="sxs-lookup"><span data-stu-id="954d3-114">-Name</span></span>
<span data-ttu-id="954d3-115">이름입니다.</span><span class="sxs-lookup"><span data-stu-id="954d3-115">Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="954d3-116">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="954d3-116">-ProtectedSetting</span></span>
<span data-ttu-id="954d3-117">VM으로 전송되기 전에 암호화된 확장에 대한 보호된 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="954d3-117">Protected settings for the extension which are encrypted before sent to the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="954d3-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="954d3-118">-Publisher</span></span>
<span data-ttu-id="954d3-119">게시자.</span><span class="sxs-lookup"><span data-stu-id="954d3-119">Publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="954d3-120">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="954d3-120">-RolesAppliedTo</span></span>
<span data-ttu-id="954d3-121">RolesAppliedTo.</span><span class="sxs-lookup"><span data-stu-id="954d3-121">RolesAppliedTo.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="954d3-122">-설정</span><span class="sxs-lookup"><span data-stu-id="954d3-122">-Setting</span></span>
<span data-ttu-id="954d3-123">확장에 대한 공용 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="954d3-123">Public settings for the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="954d3-124">-Type</span><span class="sxs-lookup"><span data-stu-id="954d3-124">-Type</span></span>
<span data-ttu-id="954d3-125">입력합니다.</span><span class="sxs-lookup"><span data-stu-id="954d3-125">Type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="954d3-126">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="954d3-126">-TypeHandlerVersion</span></span>
<span data-ttu-id="954d3-127">TypeHandlerVersion.</span><span class="sxs-lookup"><span data-stu-id="954d3-127">TypeHandlerVersion.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="954d3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="954d3-128">CommonParameters</span></span>
<span data-ttu-id="954d3-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="954d3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="954d3-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="954d3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="954d3-131">입력</span><span class="sxs-lookup"><span data-stu-id="954d3-131">INPUTS</span></span>

## <span data-ttu-id="954d3-132">출력</span><span class="sxs-lookup"><span data-stu-id="954d3-132">OUTPUTS</span></span>

### <span data-ttu-id="954d3-133">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="954d3-133">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="954d3-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="954d3-134">NOTES</span></span>

<span data-ttu-id="954d3-135">별칭</span><span class="sxs-lookup"><span data-stu-id="954d3-135">ALIASES</span></span>

## <span data-ttu-id="954d3-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="954d3-136">RELATED LINKS</span></span>

