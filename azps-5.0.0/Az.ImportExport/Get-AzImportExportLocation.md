---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
ms.openlocfilehash: c603c01619128d1697256174e9d0bc00a1cea8ff
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303995"
---
# <span data-ttu-id="572a8-101">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="572a8-101">Get-AzImportExportLocation</span></span>

## <span data-ttu-id="572a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="572a8-102">SYNOPSIS</span></span>
<span data-ttu-id="572a8-103">가져오기 또는 내보내기 작업과 연결 된 디스크를 제공할 수 있는 위치에 대 한 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="572a8-103">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="572a8-104">위치는 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="572a8-104">A location is an Azure region.</span></span>

## <span data-ttu-id="572a8-105">구문과</span><span class="sxs-lookup"><span data-stu-id="572a8-105">SYNTAX</span></span>

### <span data-ttu-id="572a8-106">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="572a8-106">List (Default)</span></span>
```
Get-AzImportExportLocation [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="572a8-107">가져오기</span><span class="sxs-lookup"><span data-stu-id="572a8-107">Get</span></span>
```
Get-AzImportExportLocation -Name <String> [-AcceptLanguage <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="572a8-108">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="572a8-108">GetViaIdentity</span></span>
```
Get-AzImportExportLocation -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="572a8-109">설명은</span><span class="sxs-lookup"><span data-stu-id="572a8-109">DESCRIPTION</span></span>
<span data-ttu-id="572a8-110">가져오기 또는 내보내기 작업과 연결 된 디스크를 제공할 수 있는 위치에 대 한 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="572a8-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="572a8-111">위치는 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="572a8-111">A location is an Azure region.</span></span>

## <span data-ttu-id="572a8-112">예제의</span><span class="sxs-lookup"><span data-stu-id="572a8-112">EXAMPLES</span></span>

### <span data-ttu-id="572a8-113">예제 1: 기본 컨텍스트로 모든 Azure 지역 위치 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="572a8-113">Example 1: Get all Azure region location details with default context</span></span>
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

<span data-ttu-id="572a8-114">이 cmdlet은 기본 컨텍스트를 사용 하 여 모든 Azure 지역 위치 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="572a8-114">This cmdlet gets all Azure region location details with default context.</span></span>

### <span data-ttu-id="572a8-115">예제 2: 위치 이름으로 Azure 지역 위치 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="572a8-115">Example 2: Get Azure region location details by location name</span></span>
```powershell
PS C:\> Get-AzImportExportLocation -Name eastus
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="572a8-116">이 cmdlet은 위치 이름으로 Azure 지역 위치 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="572a8-116">This cmdlet gets Azure region location details by location name.</span></span>

### <span data-ttu-id="572a8-117">예제 3: id 별 Azure 지역 위치 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="572a8-117">Example 3: Get Azure region location details by identity</span></span>
```powershell
PS C:\> $Id = "/providers/Microsoft.ImportExport/locations/eastus"
PS C:\> Get-AzImportExportLocation -InputObject $Id
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="572a8-118">이 cmdlet 목록은 id를 기준으로 Azure 지역 위치 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="572a8-118">This cmdlet lists gets Azure region location details by identity.</span></span>

## <span data-ttu-id="572a8-119">변수</span><span class="sxs-lookup"><span data-stu-id="572a8-119">PARAMETERS</span></span>

### <span data-ttu-id="572a8-120">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="572a8-120">-AcceptLanguage</span></span>
<span data-ttu-id="572a8-121">응답의 기본 언어를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="572a8-121">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="572a8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="572a8-122">-DefaultProfile</span></span>
<span data-ttu-id="572a8-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="572a8-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="572a8-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="572a8-124">-InputObject</span></span>
<span data-ttu-id="572a8-125">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="572a8-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="572a8-126">-이름</span><span class="sxs-lookup"><span data-stu-id="572a8-126">-Name</span></span>
<span data-ttu-id="572a8-127">위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="572a8-127">The name of the location.</span></span>
<span data-ttu-id="572a8-128">예를 들어 미국/동 또는 westus.</span><span class="sxs-lookup"><span data-stu-id="572a8-128">For example, West US or westus.</span></span>

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

### <span data-ttu-id="572a8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="572a8-129">CommonParameters</span></span>
<span data-ttu-id="572a8-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="572a8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="572a8-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="572a8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="572a8-132">입력</span><span class="sxs-lookup"><span data-stu-id="572a8-132">INPUTS</span></span>

### <span data-ttu-id="572a8-133">IImportExportIdentity 내보내기. i m a.</span><span class="sxs-lookup"><span data-stu-id="572a8-133">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="572a8-134">출력</span><span class="sxs-lookup"><span data-stu-id="572a8-134">OUTPUTS</span></span>

### <span data-ttu-id="572a8-135">Api20161101. ILocation의. PowerShell for.</span><span class="sxs-lookup"><span data-stu-id="572a8-135">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation</span></span>

## <span data-ttu-id="572a8-136">상속자</span><span class="sxs-lookup"><span data-stu-id="572a8-136">NOTES</span></span>

<span data-ttu-id="572a8-137">별칭과</span><span class="sxs-lookup"><span data-stu-id="572a8-137">ALIASES</span></span>

<span data-ttu-id="572a8-138">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="572a8-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="572a8-139">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="572a8-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="572a8-140">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="572a8-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="572a8-141">INPUTOBJECT <IImportExportIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="572a8-141">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="572a8-142">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="572a8-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="572a8-143">`[JobName <String>]`: 가져오기/내보내기 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="572a8-143">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="572a8-144">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="572a8-144">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="572a8-145">예를 들어 미국/동 또는 westus.</span><span class="sxs-lookup"><span data-stu-id="572a8-145">For example, West US or westus.</span></span>
  - <span data-ttu-id="572a8-146">`[ResourceGroupName <String>]`: 리소스 그룹 이름은 사용자 구독 내에서 리소스 그룹을 고유 하 게 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="572a8-146">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="572a8-147">`[SubscriptionId <String>]`: Azure 사용자의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="572a8-147">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="572a8-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="572a8-148">RELATED LINKS</span></span>

