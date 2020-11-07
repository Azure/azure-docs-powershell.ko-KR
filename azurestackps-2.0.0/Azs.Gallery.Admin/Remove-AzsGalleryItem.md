---
external help file: ''
Module Name: Azs.Gallery.Admin
online version: https://docs.microsoft.com/powershell/module/azs.gallery.admin/remove-azsgalleryitem
schema: 2.0.0
ms.openlocfilehash: c39a6cd64f48a7d8d6657499357daa1dd70fc091
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876048"
---
# <span data-ttu-id="41a53-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="41a53-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="41a53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41a53-102">SYNOPSIS</span></span>
<span data-ttu-id="41a53-103">특정 갤러리 항목을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="41a53-104">구문과</span><span class="sxs-lookup"><span data-stu-id="41a53-104">SYNTAX</span></span>

### <span data-ttu-id="41a53-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="41a53-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem -Name <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="41a53-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="41a53-106">DeleteViaIdentity</span></span>
```
Remove-AzsGalleryItem -InputObject <IGalleryIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="41a53-107">설명은</span><span class="sxs-lookup"><span data-stu-id="41a53-107">DESCRIPTION</span></span>
<span data-ttu-id="41a53-108">특정 갤러리 항목을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="41a53-109">예제의</span><span class="sxs-lookup"><span data-stu-id="41a53-109">EXAMPLES</span></span>

### <span data-ttu-id="41a53-110">예제 1: Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="41a53-110">Example 1: Remove-AzsGalleryItem</span></span>
```powershell
PS C:\> Remove-AzsGalleryItem -Name TestUbuntu.Test.1.0.0

```

<span data-ttu-id="41a53-111">Azure 스택 갤러리에서 TestUbuntu를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-111">Deletes TestUbuntu.Test.1.0.0 from Azure Stack gallery.</span></span>

### <span data-ttu-id="41a53-112">예제 2: 파이프라인을 통해 Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="41a53-112">Example 2: Remove-AzsGalleryItem through pipeline</span></span>
```powershell
PS C:\> Get-AzsGalleryItem -Name TestUbuntu.Test.1.0.0 | Remove-AzsGalleryItem

```

<span data-ttu-id="41a53-113">파이프라인을 통해 TestUbuntu를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-113">Deletes TestUbuntu.Test.1.0.0 through pipeline.</span></span>

## <span data-ttu-id="41a53-114">변수</span><span class="sxs-lookup"><span data-stu-id="41a53-114">PARAMETERS</span></span>

### <span data-ttu-id="41a53-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41a53-115">-DefaultProfile</span></span>
<span data-ttu-id="41a53-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41a53-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41a53-117">-InputObject</span></span>
<span data-ttu-id="41a53-118">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="41a53-119">-이름</span><span class="sxs-lookup"><span data-stu-id="41a53-119">-Name</span></span>
<span data-ttu-id="41a53-120">갤러리 항목의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-120">Identity of the gallery item.</span></span>
<span data-ttu-id="41a53-121">Publisher 이름, 항목 이름 등을 포함 하며 기간으로 구분 된 버전을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-121">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: GalleryItemName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="41a53-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41a53-122">-PassThru</span></span>
<span data-ttu-id="41a53-123">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="41a53-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="41a53-124">-SubscriptionId</span></span>
<span data-ttu-id="41a53-125">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="41a53-126">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-126">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="41a53-127">-확인</span><span class="sxs-lookup"><span data-stu-id="41a53-127">-Confirm</span></span>
<span data-ttu-id="41a53-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41a53-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41a53-129">-WhatIf</span></span>
<span data-ttu-id="41a53-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41a53-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41a53-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41a53-132">CommonParameters</span></span>
<span data-ttu-id="41a53-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41a53-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="41a53-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41a53-135">입력</span><span class="sxs-lookup"><span data-stu-id="41a53-135">INPUTS</span></span>

### <span data-ttu-id="41a53-136">IGalleryIdentity (Microsoft. PowerShell. 모델)</span><span class="sxs-lookup"><span data-stu-id="41a53-136">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity</span></span>

## <span data-ttu-id="41a53-137">출력</span><span class="sxs-lookup"><span data-stu-id="41a53-137">OUTPUTS</span></span>

### <span data-ttu-id="41a53-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="41a53-138">System.Boolean</span></span>



## <span data-ttu-id="41a53-139">상속자</span><span class="sxs-lookup"><span data-stu-id="41a53-139">NOTES</span></span>

<span data-ttu-id="41a53-140">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="41a53-141">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="41a53-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="41a53-142">INPUTOBJECT <IGalleryIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="41a53-142">INPUTOBJECT <IGalleryIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="41a53-143">`[GalleryItemName <String>]`: 갤러리 항목의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-143">`[GalleryItemName <String>]`: Identity of the gallery item.</span></span> <span data-ttu-id="41a53-144">Publisher 이름, 항목 이름 등을 포함 하며 기간으로 구분 된 버전을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-144">Includes publisher name, item name, and may include version separated by period character.</span></span>
  - <span data-ttu-id="41a53-145">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="41a53-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="41a53-146">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-146">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="41a53-147">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-147">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="41a53-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41a53-148">RELATED LINKS</span></span>

