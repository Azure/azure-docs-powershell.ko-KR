---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BB216903-B2BB-4948-AC28-408ED6C768F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6cae249f99282006ff8636e8d727485a223e2a1d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045899"
---
# <span data-ttu-id="b502b-101">New-AzureService</span><span class="sxs-lookup"><span data-stu-id="b502b-101">New-AzureService</span></span>

## <span data-ttu-id="b502b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b502b-102">SYNOPSIS</span></span>
<span data-ttu-id="b502b-103">Azure 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b502b-103">Creates an Azure service.</span></span>

## <span data-ttu-id="b502b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b502b-104">SYNTAX</span></span>

### <span data-ttu-id="b502b-105">ParameterSetAffinityGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="b502b-105">ParameterSetAffinityGroup (Default)</span></span>
```
New-AzureService [-ServiceName] <String> [-AffinityGroup] <String> [[-Label] <String>]
 [[-Description] <String>] [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b502b-106">ParameterSetLocation</span><span class="sxs-lookup"><span data-stu-id="b502b-106">ParameterSetLocation</span></span>
```
New-AzureService [-ServiceName] <String> [-Location] <String> [[-Label] <String>] [[-Description] <String>]
 [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b502b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b502b-107">DESCRIPTION</span></span>
<span data-ttu-id="b502b-108">**새로운 azureservice** cmdlet은 현재 구독에 새 Azure 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b502b-108">The **New-AzureService** cmdlet creates a new Azure service in the current subscription.</span></span>

## <span data-ttu-id="b502b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b502b-109">EXAMPLES</span></span>

### <span data-ttu-id="b502b-110">예제 1: 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="b502b-110">Example 1: Create a service</span></span>
```
PS C:\> New-AzureService -ServiceName "MySvc01" -Label "MyTestService" -Location "South Central US"
```

<span data-ttu-id="b502b-111">이 명령은 미국 중앙 US 위치에 MySvc01 이라는 새 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b502b-111">This command creates a new service named MySvc01 in the South Central US location.</span></span>

### <span data-ttu-id="b502b-112">예제 2: 선호도 그룹에서 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="b502b-112">Example 2: Create a service in an affinity group</span></span>
```
PS C:\> New-AzureService -ServiceName "MySvc01" -AffinityGroup NorthRegion
```

<span data-ttu-id="b502b-113">이 명령은 NorthRegion affinity 그룹을 사용 하 여 MySvc01 이라는 새 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b502b-113">This command creates a new service named MySvc01 using the NorthRegion affinity group.</span></span>

## <span data-ttu-id="b502b-114">변수</span><span class="sxs-lookup"><span data-stu-id="b502b-114">PARAMETERS</span></span>

### <span data-ttu-id="b502b-115">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="b502b-115">-AffinityGroup</span></span>
<span data-ttu-id="b502b-116">구독과 연결 된 선호도 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b502b-116">Specifies the affinity group associated with the subscription.</span></span>
<span data-ttu-id="b502b-117">*위치* 매개 변수를 지정 하지 않으면 선호도 그룹이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b502b-117">If you do not specify the *Location* parameter, an affinity group is required.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetAffinityGroup
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b502b-118">-설명</span><span class="sxs-lookup"><span data-stu-id="b502b-118">-Description</span></span>
<span data-ttu-id="b502b-119">서비스에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b502b-119">Specifies a description for the service.</span></span>
<span data-ttu-id="b502b-120">설명은 최대 1024 자를 초과할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b502b-120">The description may be up to 1024 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b502b-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b502b-121">-InformationAction</span></span>
<span data-ttu-id="b502b-122">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b502b-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b502b-123">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b502b-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b502b-124">하기로</span><span class="sxs-lookup"><span data-stu-id="b502b-124">Continue</span></span>
- <span data-ttu-id="b502b-125">숨기기</span><span class="sxs-lookup"><span data-stu-id="b502b-125">Ignore</span></span>
- <span data-ttu-id="b502b-126">Inquire</span><span class="sxs-lookup"><span data-stu-id="b502b-126">Inquire</span></span>
- <span data-ttu-id="b502b-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b502b-127">SilentlyContinue</span></span>
- <span data-ttu-id="b502b-128">중지가</span><span class="sxs-lookup"><span data-stu-id="b502b-128">Stop</span></span>
- <span data-ttu-id="b502b-129">대기</span><span class="sxs-lookup"><span data-stu-id="b502b-129">Suspend</span></span>

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

### <span data-ttu-id="b502b-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b502b-130">-InformationVariable</span></span>
<span data-ttu-id="b502b-131">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b502b-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b502b-132">-레이블</span><span class="sxs-lookup"><span data-stu-id="b502b-132">-Label</span></span>
<span data-ttu-id="b502b-133">서비스에 대 한 레이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b502b-133">Specifies a label for the service.</span></span>
<span data-ttu-id="b502b-134">레이블은 최대 100 자를 초과할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b502b-134">The label may be up to 100 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b502b-135">-위치</span><span class="sxs-lookup"><span data-stu-id="b502b-135">-Location</span></span>
<span data-ttu-id="b502b-136">서비스의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b502b-136">Specifies the location for the service.</span></span>
<span data-ttu-id="b502b-137">지정 된 선호도 그룹이 없는 경우 위치가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b502b-137">A location is required if there isn't a specified Affinity Group.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetLocation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b502b-138">-프로필</span><span class="sxs-lookup"><span data-stu-id="b502b-138">-Profile</span></span>
<span data-ttu-id="b502b-139">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b502b-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b502b-140">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b502b-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b502b-141">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="b502b-141">-ReverseDnsFqdn</span></span>
<span data-ttu-id="b502b-142">역방향 DNS에 대해 정규화 된 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b502b-142">Specifies the fully qualified domain name for reverse DNS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b502b-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b502b-143">-ServiceName</span></span>
<span data-ttu-id="b502b-144">새 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b502b-144">Specifies the name of the new service.</span></span>
<span data-ttu-id="b502b-145">이름은 구독에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b502b-145">The name must be unique to the subscription.</span></span>

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

### <span data-ttu-id="b502b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b502b-146">CommonParameters</span></span>
<span data-ttu-id="b502b-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b502b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b502b-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b502b-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b502b-149">입력</span><span class="sxs-lookup"><span data-stu-id="b502b-149">INPUTS</span></span>

## <span data-ttu-id="b502b-150">출력</span><span class="sxs-lookup"><span data-stu-id="b502b-150">OUTPUTS</span></span>

## <span data-ttu-id="b502b-151">상속자</span><span class="sxs-lookup"><span data-stu-id="b502b-151">NOTES</span></span>

## <span data-ttu-id="b502b-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b502b-152">RELATED LINKS</span></span>

[<span data-ttu-id="b502b-153">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="b502b-153">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="b502b-154">Set AzureService</span><span class="sxs-lookup"><span data-stu-id="b502b-154">Set-AzureService</span></span>](./Set-AzureService.md)


