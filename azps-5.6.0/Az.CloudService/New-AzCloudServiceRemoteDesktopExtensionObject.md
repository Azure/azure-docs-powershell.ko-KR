---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-azcloudserviceremotedesktopextensionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRemoteDesktopExtensionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRemoteDesktopExtensionObject.md
ms.openlocfilehash: 5ae7383f71524c87518b9f48cbb314bf74de633e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998214"
---
# <span data-ttu-id="3e666-101">New-AzCloudServiceRemoteDesktopExtensionObject</span><span class="sxs-lookup"><span data-stu-id="3e666-101">New-AzCloudServiceRemoteDesktopExtensionObject</span></span>

## <span data-ttu-id="3e666-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e666-102">SYNOPSIS</span></span>
<span data-ttu-id="3e666-103">원격 데스크톱 확장에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="3e666-103">Create a in-memory object for Remote Desktop Extension</span></span>

## <span data-ttu-id="3e666-104">구문</span><span class="sxs-lookup"><span data-stu-id="3e666-104">SYNTAX</span></span>

```
New-AzCloudServiceRemoteDesktopExtensionObject [-Name] <String> [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-TypeHandlerVersion] <String>] [[-RolesAppliedTo] <String[]>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [<CommonParameters>]
```

## <span data-ttu-id="3e666-105">설명</span><span class="sxs-lookup"><span data-stu-id="3e666-105">DESCRIPTION</span></span>
<span data-ttu-id="3e666-106">원격 데스크톱 확장에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="3e666-106">Create a in-memory object for Remote Desktop Extension</span></span>

## <span data-ttu-id="3e666-107">예제</span><span class="sxs-lookup"><span data-stu-id="3e666-107">EXAMPLES</span></span>

### <span data-ttu-id="3e666-108">예제 1: 원격 데스크톱 확장 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="3e666-108">Example 1: Create remote desktop extension object</span></span>
```powershell
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $extension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'
```

<span data-ttu-id="3e666-109">이 명령은 클라우드 서비스를 만들거나 업데이트하는 데 사용되는 원격 데스크톱 확장 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3e666-109">This command creates remote desktop extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="3e666-110">자세한 내용은 New-AzCloudService를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="3e666-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="3e666-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3e666-111">PARAMETERS</span></span>

### <span data-ttu-id="3e666-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="3e666-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="3e666-113">자동 업그레이드 부 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="3e666-113">Auto upgrade minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e666-114">-자격 증명</span><span class="sxs-lookup"><span data-stu-id="3e666-114">-Credential</span></span>
<span data-ttu-id="3e666-115">원격 데스크톱 확장에 대한 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="3e666-115">Credential for Remote Desktop Extension.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e666-116">-만료</span><span class="sxs-lookup"><span data-stu-id="3e666-116">-Expiration</span></span>
<span data-ttu-id="3e666-117">원격 데스크톱 확장에 대한 만료입니다.</span><span class="sxs-lookup"><span data-stu-id="3e666-117">Expiration for Remote Desktop Extension.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e666-118">-Name</span><span class="sxs-lookup"><span data-stu-id="3e666-118">-Name</span></span>
<span data-ttu-id="3e666-119">원격 데스크톱 확장의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3e666-119">Name of Remote Desktop Extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e666-120">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="3e666-120">-RolesAppliedTo</span></span>
<span data-ttu-id="3e666-121">역할이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e666-121">Roles applied to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e666-122">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="3e666-122">-TypeHandlerVersion</span></span>
<span data-ttu-id="3e666-123">원격 데스크톱 확장 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="3e666-123">Remote Desktop Extension version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e666-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e666-124">CommonParameters</span></span>
<span data-ttu-id="3e666-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3e666-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e666-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e666-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e666-127">입력</span><span class="sxs-lookup"><span data-stu-id="3e666-127">INPUTS</span></span>

## <span data-ttu-id="3e666-128">출력</span><span class="sxs-lookup"><span data-stu-id="3e666-128">OUTPUTS</span></span>

### <span data-ttu-id="3e666-129">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="3e666-129">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="3e666-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3e666-130">NOTES</span></span>

<span data-ttu-id="3e666-131">별칭</span><span class="sxs-lookup"><span data-stu-id="3e666-131">ALIASES</span></span>

## <span data-ttu-id="3e666-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3e666-132">RELATED LINKS</span></span>

