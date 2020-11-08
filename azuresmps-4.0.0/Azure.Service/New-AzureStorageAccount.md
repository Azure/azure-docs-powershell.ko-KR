---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 931BC75D-B8EF-463D-8FCE-A822093CB05A
online version: ''
schema: 2.0.0
ms.openlocfilehash: bbc1963dbf56d0ef7f31d2174ab352dcc36af619
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046204"
---
# <span data-ttu-id="e883f-101">New-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e883f-101">New-AzureStorageAccount</span></span>

## <span data-ttu-id="e883f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e883f-102">SYNOPSIS</span></span>
<span data-ttu-id="e883f-103">Azure 구독에서 새 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e883f-103">Creates a new storage account in an Azure subscription.</span></span>

## <span data-ttu-id="e883f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e883f-104">SYNTAX</span></span>

### <span data-ttu-id="e883f-105">ParameterSetAffinityGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="e883f-105">ParameterSetAffinityGroup (Default)</span></span>
```
New-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 -AffinityGroup <String> [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e883f-106">ParameterSetLocation</span><span class="sxs-lookup"><span data-stu-id="e883f-106">ParameterSetLocation</span></span>
```
New-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 -Location <String> [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e883f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e883f-107">DESCRIPTION</span></span>
<span data-ttu-id="e883f-108">**새-AzureStorageAccount** Cmdlet은 Azure 저장소 서비스에 대 한 액세스를 제공 하는 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e883f-108">The **New-AzureStorageAccount** cmdlet creates an account that provides access to Azure storage services.</span></span>
<span data-ttu-id="e883f-109">저장소 계정은 저장소 시스템 내의 전역적으로 고유한 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="e883f-109">A storage account is a globally unique resource within the storage system.</span></span>
<span data-ttu-id="e883f-110">계정은 Blob, 큐 및 테이블 서비스의 상위 네임 스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="e883f-110">The account is the parent namespace for the Blob, Queue, and Table services.</span></span>

## <span data-ttu-id="e883f-111">예제의</span><span class="sxs-lookup"><span data-stu-id="e883f-111">EXAMPLES</span></span>

### <span data-ttu-id="e883f-112">예제 1: 지정 된 선호도 그룹에 대 한 저장소 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="e883f-112">Example 1: Create a storage account for a specified affinity group</span></span>
```
PS C:\> New-AzureStorageAccount -StorageAccountName "azure01" -Label "AzureOne" -AffinityGroup "prodapps"
```

<span data-ttu-id="e883f-113">이 명령은 지정 된 선호도 그룹에 대 한 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e883f-113">This command creates a storage account for a specified affinity group.</span></span>

### <span data-ttu-id="e883f-114">예제 2: 지정 된 위치에 저장소 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="e883f-114">Example 2: Create a storage account in a specified location</span></span>
```
PS C:\> New-AzureStorageAccount -StorageAccountName "azure02" -Label "AzureTwo" -Location "North Central US"
```

<span data-ttu-id="e883f-115">이 명령은 지정 된 위치에 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e883f-115">This command creates a storage account in a specified location.</span></span>

## <span data-ttu-id="e883f-116">변수</span><span class="sxs-lookup"><span data-stu-id="e883f-116">PARAMETERS</span></span>

### <span data-ttu-id="e883f-117">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="e883f-117">-AffinityGroup</span></span>
<span data-ttu-id="e883f-118">현재 구독에 있는 기존 선호도 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e883f-118">Specifies the name of an existing affinity group in the current subscription.</span></span>
<span data-ttu-id="e883f-119">*Location* 또는 *AffinityGroup* 매개 변수 중 하나만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e883f-119">You can specify either the *Location* or *AffinityGroup* parameter, but not both.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetAffinityGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e883f-120">-설명</span><span class="sxs-lookup"><span data-stu-id="e883f-120">-Description</span></span>
<span data-ttu-id="e883f-121">저장소 계정에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e883f-121">Specifies a description for the storage account.</span></span>
<span data-ttu-id="e883f-122">설명은 최대 1024 자를 초과할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e883f-122">The description may be up to 1024 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e883f-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e883f-123">-InformationAction</span></span>
<span data-ttu-id="e883f-124">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e883f-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e883f-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e883f-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e883f-126">하기로</span><span class="sxs-lookup"><span data-stu-id="e883f-126">Continue</span></span>
- <span data-ttu-id="e883f-127">숨기기</span><span class="sxs-lookup"><span data-stu-id="e883f-127">Ignore</span></span>
- <span data-ttu-id="e883f-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="e883f-128">Inquire</span></span>
- <span data-ttu-id="e883f-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e883f-129">SilentlyContinue</span></span>
- <span data-ttu-id="e883f-130">중지가</span><span class="sxs-lookup"><span data-stu-id="e883f-130">Stop</span></span>
- <span data-ttu-id="e883f-131">대기</span><span class="sxs-lookup"><span data-stu-id="e883f-131">Suspend</span></span>

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

### <span data-ttu-id="e883f-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e883f-132">-InformationVariable</span></span>
<span data-ttu-id="e883f-133">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e883f-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e883f-134">-레이블</span><span class="sxs-lookup"><span data-stu-id="e883f-134">-Label</span></span>
<span data-ttu-id="e883f-135">저장소 계정에 대 한 레이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e883f-135">Specifies a label for the storage account.</span></span>
<span data-ttu-id="e883f-136">레이블은 최대 100 자를 초과할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e883f-136">The label may be up to 100 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e883f-137">-위치</span><span class="sxs-lookup"><span data-stu-id="e883f-137">-Location</span></span>
<span data-ttu-id="e883f-138">저장소 계정이 만들어지는 Azure 데이터 센터 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e883f-138">Specifies the Azure data center location where the storage account is created.</span></span>
<span data-ttu-id="e883f-139">*Location* 또는 *AffinityGroup* 매개 변수 중 하나만 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e883f-139">You can include either the *Location* or *AffinityGroup* parameter, but not both.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e883f-140">-프로필</span><span class="sxs-lookup"><span data-stu-id="e883f-140">-Profile</span></span>
<span data-ttu-id="e883f-141">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e883f-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e883f-142">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e883f-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e883f-143">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e883f-143">-StorageAccountName</span></span>
<span data-ttu-id="e883f-144">저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e883f-144">Specifies a name for the storage account.</span></span>
<span data-ttu-id="e883f-145">저장소 계정 이름은 Azure에서 고유 해야 하며 3 ~ 24 자 사이 여야 하 고 소문자와 숫자만 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e883f-145">The storage account name must be unique to Azure and must be between 3 and 24 characters in length and use lowercase letters and numbers only.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e883f-146">-Type</span><span class="sxs-lookup"><span data-stu-id="e883f-146">-Type</span></span>
<span data-ttu-id="e883f-147">저장소 계정의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e883f-147">Specifies the type of the storage account.</span></span>
<span data-ttu-id="e883f-148">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e883f-148">Valid values are:</span></span>

- <span data-ttu-id="e883f-149">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="e883f-149">Standard_LRS</span></span>
- <span data-ttu-id="e883f-150">Standard_ZRS</span><span class="sxs-lookup"><span data-stu-id="e883f-150">Standard_ZRS</span></span>
- <span data-ttu-id="e883f-151">Standard_GRS</span><span class="sxs-lookup"><span data-stu-id="e883f-151">Standard_GRS</span></span>
- <span data-ttu-id="e883f-152">Standard_RAGRS</span><span class="sxs-lookup"><span data-stu-id="e883f-152">Standard_RAGRS</span></span>
- <span data-ttu-id="e883f-153">Premium_LRS</span><span class="sxs-lookup"><span data-stu-id="e883f-153">Premium_LRS</span></span>

<span data-ttu-id="e883f-154">이 매개 변수를 지정 하지 않을 경우 기본값은 Standard_GRS입니다.</span><span class="sxs-lookup"><span data-stu-id="e883f-154">If this parameter is not specified, the default value is Standard_GRS.</span></span>

<span data-ttu-id="e883f-155">Standard_ZRS 또는 Premium_LRS 계정은 다른 계정 유형으로 변경 하거나 그 반대의 경우도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="e883f-155">Standard_ZRS or Premium_LRS accounts cannot be changed to other account types, and vice versa.</span></span>

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

### <span data-ttu-id="e883f-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e883f-156">CommonParameters</span></span>
<span data-ttu-id="e883f-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e883f-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e883f-158">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e883f-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e883f-159">입력</span><span class="sxs-lookup"><span data-stu-id="e883f-159">INPUTS</span></span>

## <span data-ttu-id="e883f-160">출력</span><span class="sxs-lookup"><span data-stu-id="e883f-160">OUTPUTS</span></span>

## <span data-ttu-id="e883f-161">상속자</span><span class="sxs-lookup"><span data-stu-id="e883f-161">NOTES</span></span>

## <span data-ttu-id="e883f-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e883f-162">RELATED LINKS</span></span>

[<span data-ttu-id="e883f-163">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e883f-163">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="e883f-164">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e883f-164">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


