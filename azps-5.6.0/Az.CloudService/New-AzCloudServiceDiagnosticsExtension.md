---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/new-azcloudservicediagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceDiagnosticsExtension.md
ms.openlocfilehash: a87e9c76b2c083392fc37d74a3ba213dba5881ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969611"
---
# <span data-ttu-id="cba26-101">New-AzCloudServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="cba26-101">New-AzCloudServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="cba26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cba26-102">SYNOPSIS</span></span>
<span data-ttu-id="cba26-103">진단 확장에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="cba26-103">Create a in-memory object for Diagnostics Extension</span></span>

## <span data-ttu-id="cba26-104">구문</span><span class="sxs-lookup"><span data-stu-id="cba26-104">SYNTAX</span></span>

```
New-AzCloudServiceDiagnosticsExtension [-Name] <String> [-ResourceGroupName] <String>
 [-CloudServiceName] <String> [-DiagnosticsConfigurationPath] <String> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [[-Subscription] <String>] [[-TypeHandlerVersion] <String>]
 [[-RolesAppliedTo] <String[]>] [[-AutoUpgradeMinorVersion] <Boolean>] [<CommonParameters>]
```

## <span data-ttu-id="cba26-105">설명</span><span class="sxs-lookup"><span data-stu-id="cba26-105">DESCRIPTION</span></span>
<span data-ttu-id="cba26-106">진단 확장에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="cba26-106">Create a in-memory object for Diagnostics Extension</span></span>

## <span data-ttu-id="cba26-107">예제</span><span class="sxs-lookup"><span data-stu-id="cba26-107">EXAMPLES</span></span>

### <span data-ttu-id="cba26-108">예제 1: 진단 확장 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="cba26-108">Example 1: Create diagnostics extension object</span></span>
```powershell
PS C:\> $storageAccountKey = Get-AzStorageAccountKey -ResourceGroupName "ContosOrg" -Name "ContosSA"
PS C:\> $configFile = "<WAD configuration file path>"
PS C:\> $extension = New-AzCloudServiceDiagnosticsExtension -Name "WADExtension" -ResourceGroupName "ContosOrg" -CloudServiceName "ContosCS" -StorageAccountName "ContosSA" -StorageAccountKey $storageAccountKey[0].Value -DiagnosticsConfigurationPath $configFile -TypeHandlerVersion "1.5" -AutoUpgradeMinorVersion $true
```

<span data-ttu-id="cba26-109">이 명령은 클라우드 서비스를 만들거나 업데이트하는 데 사용되는 진단 확장 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cba26-109">This command creates diagnostics extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="cba26-110">자세한 내용은 New-AzCloudService를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="cba26-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="cba26-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cba26-111">PARAMETERS</span></span>

### <span data-ttu-id="cba26-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="cba26-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="cba26-113">자동 업그레이드 부 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="cba26-113">Auto upgrade minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba26-114">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="cba26-114">-CloudServiceName</span></span>
<span data-ttu-id="cba26-115">클라우드 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cba26-115">Name of Cloud Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba26-116">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="cba26-116">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="cba26-117">Azure Diagnostics에 대한 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cba26-117">Specifies the configuration for Azure Diagnostics.</span></span>
<span data-ttu-id="cba26-118">다음 명령을 사용하여 (Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics')를 사용하여 해당 스케마를 다운로드할 수 있습니다. PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'</span><span class="sxs-lookup"><span data-stu-id="cba26-118">You can download the schema by using the following command: (Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics').PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba26-119">-Name</span><span class="sxs-lookup"><span data-stu-id="cba26-119">-Name</span></span>
<span data-ttu-id="cba26-120">진단 확장의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cba26-120">Name of Diagnostics Extension.</span></span>

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

### <span data-ttu-id="cba26-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cba26-121">-ResourceGroupName</span></span>
<span data-ttu-id="cba26-122">Cloud Service의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cba26-122">Resource Group name of Cloud Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba26-123">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="cba26-123">-RolesAppliedTo</span></span>
<span data-ttu-id="cba26-124">역할이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="cba26-124">Roles applied to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba26-125">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="cba26-125">-StorageAccountKey</span></span>
<span data-ttu-id="cba26-126">저장소 계정 키입니다.</span><span class="sxs-lookup"><span data-stu-id="cba26-126">Storage Account Key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba26-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cba26-127">-StorageAccountName</span></span>
<span data-ttu-id="cba26-128">Storage 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cba26-128">Name of the Storage Account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba26-129">-Subscription</span><span class="sxs-lookup"><span data-stu-id="cba26-129">-Subscription</span></span>
<span data-ttu-id="cba26-130">구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cba26-130">Subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba26-131">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="cba26-131">-TypeHandlerVersion</span></span>
<span data-ttu-id="cba26-132">확장의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cba26-132">Specifies the version of the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba26-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cba26-133">CommonParameters</span></span>
<span data-ttu-id="cba26-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cba26-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cba26-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cba26-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cba26-136">입력</span><span class="sxs-lookup"><span data-stu-id="cba26-136">INPUTS</span></span>

## <span data-ttu-id="cba26-137">출력</span><span class="sxs-lookup"><span data-stu-id="cba26-137">OUTPUTS</span></span>

### <span data-ttu-id="cba26-138">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="cba26-138">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="cba26-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cba26-139">NOTES</span></span>

<span data-ttu-id="cba26-140">별칭</span><span class="sxs-lookup"><span data-stu-id="cba26-140">ALIASES</span></span>

## <span data-ttu-id="cba26-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cba26-141">RELATED LINKS</span></span>

