---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 54C89A5F-BF94-468C-92E7-224808FDD0EC
online version: ''
schema: 2.0.0
ms.openlocfilehash: be84995e4826b79befc6282133d70f3ee4a79b4f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046227"
---
# <span data-ttu-id="91a83-101">New-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="91a83-101">New-AzureAffinityGroup</span></span>

## <span data-ttu-id="91a83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91a83-102">SYNOPSIS</span></span>
<span data-ttu-id="91a83-103">현재 구독에서 선호도 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91a83-103">Creates an affinity group in the current subscription.</span></span>

## <span data-ttu-id="91a83-104">구문과</span><span class="sxs-lookup"><span data-stu-id="91a83-104">SYNTAX</span></span>

```
New-AzureAffinityGroup [-Name] <String> [-Label <String>] [-Description <String>] -Location <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="91a83-105">설명은</span><span class="sxs-lookup"><span data-stu-id="91a83-105">DESCRIPTION</span></span>
<span data-ttu-id="91a83-106">**AzureAffinityGroup** cmdlet은 현재 azure 구독에서 azure 선호도 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91a83-106">The **New-AzureAffinityGroup** cmdlet creates an Azure affinity group in the current Azure subscription.</span></span>

<span data-ttu-id="91a83-107">선호도 그룹은 Azure datacenter에 서비스와 리소스를 함께 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="91a83-107">An affinity group puts your services and their resources together in an Azure datacenter.</span></span>
<span data-ttu-id="91a83-108">선호도 그룹은 최적의 성능을 위해 구성원을 함께 그룹화 합니다.</span><span class="sxs-lookup"><span data-stu-id="91a83-108">The affinity group groups members together for optimal performance.</span></span>
<span data-ttu-id="91a83-109">구독 수준에서 선호도 그룹을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="91a83-109">Define affinity groups at the subscription level.</span></span>
<span data-ttu-id="91a83-110">사용자가 만든 모든 후속 클라우드 서비스 또는 저장소 계정에서 선호도 그룹을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91a83-110">Your affinity groups are available to any subsequent cloud services or storage accounts that you create.</span></span>
<span data-ttu-id="91a83-111">선호도 그룹을 만들 때만 해당 서비스를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91a83-111">You can add services to an affinity group only when you create it.</span></span>

## <span data-ttu-id="91a83-112">예제의</span><span class="sxs-lookup"><span data-stu-id="91a83-112">EXAMPLES</span></span>

### <span data-ttu-id="91a83-113">예제 1: 선호도 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="91a83-113">Example 1: Create an affinity group</span></span>
```
PS C:\> New-AzureAffinityGroup -Name "South01" -Location "South Central US" -Label "South Region" -Description "Affinity group for production applications in southern region."
```

<span data-ttu-id="91a83-114">이 명령은 동남 중부 US 지역에서 South01 이라는 선호도 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91a83-114">This command creates an affinity group named South01 in the South Central US region.</span></span>
<span data-ttu-id="91a83-115">명령에서 레이블과 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91a83-115">The command specifies a label and a description.</span></span>

## <span data-ttu-id="91a83-116">변수</span><span class="sxs-lookup"><span data-stu-id="91a83-116">PARAMETERS</span></span>

### <span data-ttu-id="91a83-117">-설명</span><span class="sxs-lookup"><span data-stu-id="91a83-117">-Description</span></span>
<span data-ttu-id="91a83-118">선호도 그룹에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91a83-118">Specifies a description for the affinity group.</span></span>
<span data-ttu-id="91a83-119">설명은 최대 1024 자를 초과할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91a83-119">The description may be up to 1024 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a83-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="91a83-120">-InformationAction</span></span>
<span data-ttu-id="91a83-121">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91a83-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="91a83-122">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="91a83-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="91a83-123">하기로</span><span class="sxs-lookup"><span data-stu-id="91a83-123">Continue</span></span>
- <span data-ttu-id="91a83-124">숨기기</span><span class="sxs-lookup"><span data-stu-id="91a83-124">Ignore</span></span>
- <span data-ttu-id="91a83-125">Inquire</span><span class="sxs-lookup"><span data-stu-id="91a83-125">Inquire</span></span>
- <span data-ttu-id="91a83-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="91a83-126">SilentlyContinue</span></span>
- <span data-ttu-id="91a83-127">중지가</span><span class="sxs-lookup"><span data-stu-id="91a83-127">Stop</span></span>
- <span data-ttu-id="91a83-128">대기</span><span class="sxs-lookup"><span data-stu-id="91a83-128">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a83-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="91a83-129">-InformationVariable</span></span>
<span data-ttu-id="91a83-130">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91a83-130">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a83-131">-레이블</span><span class="sxs-lookup"><span data-stu-id="91a83-131">-Label</span></span>
<span data-ttu-id="91a83-132">선호도 그룹의 레이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91a83-132">Specifies a label for the affinity group.</span></span>
<span data-ttu-id="91a83-133">레이블은 최대 100 자를 초과할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91a83-133">The label may be up to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a83-134">-위치</span><span class="sxs-lookup"><span data-stu-id="91a83-134">-Location</span></span>
<span data-ttu-id="91a83-135">이 cmdlet이 선호도 그룹을 만드는 Azure 데이터 센터의 지리적 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91a83-135">Specifies the geographical location of the Azure datacenter where this cmdlet creates the affinity group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a83-136">-이름</span><span class="sxs-lookup"><span data-stu-id="91a83-136">-Name</span></span>
<span data-ttu-id="91a83-137">선호도 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91a83-137">Specifies a name for the affinity group.</span></span>
<span data-ttu-id="91a83-138">이름은 구독에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91a83-138">The name must be unique to the subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91a83-139">-프로필</span><span class="sxs-lookup"><span data-stu-id="91a83-139">-Profile</span></span>
<span data-ttu-id="91a83-140">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91a83-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="91a83-141">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="91a83-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a83-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91a83-142">CommonParameters</span></span>
<span data-ttu-id="91a83-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="91a83-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91a83-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91a83-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91a83-145">입력</span><span class="sxs-lookup"><span data-stu-id="91a83-145">INPUTS</span></span>

## <span data-ttu-id="91a83-146">출력</span><span class="sxs-lookup"><span data-stu-id="91a83-146">OUTPUTS</span></span>

## <span data-ttu-id="91a83-147">상속자</span><span class="sxs-lookup"><span data-stu-id="91a83-147">NOTES</span></span>

## <span data-ttu-id="91a83-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91a83-148">RELATED LINKS</span></span>

[<span data-ttu-id="91a83-149">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="91a83-149">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="91a83-150">제거-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="91a83-150">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)

[<span data-ttu-id="91a83-151">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="91a83-151">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


