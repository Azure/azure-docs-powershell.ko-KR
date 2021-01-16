---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
ms.openlocfilehash: c603c01619128d1697256174e9d0bc00a1cea8ff
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325940"
---
# <span data-ttu-id="c40ef-101">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="c40ef-101">Get-AzImportExportLocation</span></span>

## <span data-ttu-id="c40ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c40ef-102">SYNOPSIS</span></span>
<span data-ttu-id="c40ef-103">가져오기 또는 내보내기 작업과 연결된 디스크를 배송할 수 있는 위치에 대한 세부 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c40ef-103">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="c40ef-104">위치는 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="c40ef-104">A location is an Azure region.</span></span>

## <span data-ttu-id="c40ef-105">구문</span><span class="sxs-lookup"><span data-stu-id="c40ef-105">SYNTAX</span></span>

### <span data-ttu-id="c40ef-106">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="c40ef-106">List (Default)</span></span>
```
Get-AzImportExportLocation [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c40ef-107">가져오기</span><span class="sxs-lookup"><span data-stu-id="c40ef-107">Get</span></span>
```
Get-AzImportExportLocation -Name <String> [-AcceptLanguage <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="c40ef-108">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c40ef-108">GetViaIdentity</span></span>
```
Get-AzImportExportLocation -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c40ef-109">설명</span><span class="sxs-lookup"><span data-stu-id="c40ef-109">DESCRIPTION</span></span>
<span data-ttu-id="c40ef-110">가져오기 또는 내보내기 작업과 연결된 디스크를 배송할 수 있는 위치에 대한 세부 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c40ef-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="c40ef-111">위치는 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="c40ef-111">A location is an Azure region.</span></span>

## <span data-ttu-id="c40ef-112">예제</span><span class="sxs-lookup"><span data-stu-id="c40ef-112">EXAMPLES</span></span>

### <span data-ttu-id="c40ef-113">예제 1: 기본 컨텍스트를 사용하여 모든 Azure 지역 위치 세부 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="c40ef-113">Example 1: Get all Azure region location details with default context</span></span>
```powershell
PS C:\> Get-AzImportExportLocation
Name                 Type
----                 ----
Australia East       Microsoft.ImportExport/locations
Australia Southeast  Microsoft.ImportExport/locations
Brazil South         Microsoft.ImportExport/locations
Canada Central       Microsoft.ImportExport/locations
Canada East          Microsoft.ImportExport/locations
...
West Central US      Microsoft.ImportExport/locations
West Europe          Microsoft.ImportExport/locations
West India           Microsoft.ImportExport/locations
West US              Microsoft.ImportExport/locations
West US 2            Microsoft.ImportExport/locations
```

<span data-ttu-id="c40ef-114">이 cmdlet은 기본 컨텍스트를 사용하여 모든 Azure 지역 위치 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c40ef-114">This cmdlet gets all Azure region location details with default context.</span></span>

### <span data-ttu-id="c40ef-115">예제 2: 위치 이름으로 Azure 지역 위치 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="c40ef-115">Example 2: Get Azure region location details by location name</span></span>
```powershell
PS C:\> Get-AzImportExportLocation -Name eastus
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="c40ef-116">이 cmdlet은 위치 이름으로 Azure 지역 위치 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c40ef-116">This cmdlet gets Azure region location details by location name.</span></span>

### <span data-ttu-id="c40ef-117">예제 3: ID별로 Azure 지역 위치 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="c40ef-117">Example 3: Get Azure region location details by identity</span></span>
```powershell
PS C:\> $Id = "/providers/Microsoft.ImportExport/locations/eastus"
PS C:\> Get-AzImportExportLocation -InputObject $Id
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="c40ef-118">이 cmdlet 목록은 ID별로 Azure 지역 위치 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c40ef-118">This cmdlet lists gets Azure region location details by identity.</span></span>

## <span data-ttu-id="c40ef-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c40ef-119">PARAMETERS</span></span>

### <span data-ttu-id="c40ef-120">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="c40ef-120">-AcceptLanguage</span></span>
<span data-ttu-id="c40ef-121">응답에 대한 기본 설정 언어를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c40ef-121">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="c40ef-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c40ef-122">-DefaultProfile</span></span>
<span data-ttu-id="c40ef-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c40ef-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c40ef-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c40ef-124">-InputObject</span></span>
<span data-ttu-id="c40ef-125">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="c40ef-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c40ef-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c40ef-126">-Name</span></span>
<span data-ttu-id="c40ef-127">위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c40ef-127">The name of the location.</span></span>
<span data-ttu-id="c40ef-128">예를 들어 미국 서부 또는 westus입니다.</span><span class="sxs-lookup"><span data-stu-id="c40ef-128">For example, West US or westus.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: LocationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c40ef-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c40ef-129">CommonParameters</span></span>
<span data-ttu-id="c40ef-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c40ef-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c40ef-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c40ef-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c40ef-132">입력</span><span class="sxs-lookup"><span data-stu-id="c40ef-132">INPUTS</span></span>

### <span data-ttu-id="c40ef-133">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="c40ef-133">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="c40ef-134">출력</span><span class="sxs-lookup"><span data-stu-id="c40ef-134">OUTPUTS</span></span>

### <span data-ttu-id="c40ef-135">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation</span><span class="sxs-lookup"><span data-stu-id="c40ef-135">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation</span></span>

## <span data-ttu-id="c40ef-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c40ef-136">NOTES</span></span>

<span data-ttu-id="c40ef-137">별칭</span><span class="sxs-lookup"><span data-stu-id="c40ef-137">ALIASES</span></span>

<span data-ttu-id="c40ef-138">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="c40ef-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c40ef-139">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="c40ef-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c40ef-140">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c40ef-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c40ef-141">INPUTOBJECT: <IImportExportIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="c40ef-141">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c40ef-142">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="c40ef-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c40ef-143">`[JobName <String>]`: 가져오기/내보내기 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c40ef-143">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="c40ef-144">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c40ef-144">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="c40ef-145">예를 들어 미국 서부 또는 westus입니다.</span><span class="sxs-lookup"><span data-stu-id="c40ef-145">For example, West US or westus.</span></span>
  - <span data-ttu-id="c40ef-146">`[ResourceGroupName <String>]`: 리소스 그룹 이름은 사용자 구독 내의 리소스 그룹을 고유하게 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="c40ef-146">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="c40ef-147">`[SubscriptionId <String>]`: Azure 사용자의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c40ef-147">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="c40ef-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c40ef-148">RELATED LINKS</span></span>

