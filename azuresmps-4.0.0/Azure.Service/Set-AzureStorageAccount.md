---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EB4A7F84-99E4-49B1-856D-EC0736058D23
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8cab29cd7d285d2ae1aae9c007be965e1bbf8f2f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045850"
---
# <span data-ttu-id="61568-101">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="61568-101">Set-AzureStorageAccount</span></span>

## <span data-ttu-id="61568-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61568-102">SYNOPSIS</span></span>
<span data-ttu-id="61568-103">Azure 구독에서 저장소 계정의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="61568-103">Updates the properties of a storage account in an Azure subscription.</span></span>

## <span data-ttu-id="61568-104">구문과</span><span class="sxs-lookup"><span data-stu-id="61568-104">SYNTAX</span></span>

### <span data-ttu-id="61568-105">AccountType (기본값)</span><span class="sxs-lookup"><span data-stu-id="61568-105">AccountType (Default)</span></span>
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="61568-106">GeoReplicationEnabled</span><span class="sxs-lookup"><span data-stu-id="61568-106">GeoReplicationEnabled</span></span>
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-GeoReplicationEnabled <Boolean>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="61568-107">설명은</span><span class="sxs-lookup"><span data-stu-id="61568-107">DESCRIPTION</span></span>
<span data-ttu-id="61568-108">**집합-AzureStorageAccount** cmdlet은 현재 구독에서 Azure 저장소 계정의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="61568-108">The **Set-AzureStorageAccount** cmdlet updates the properties of an Azure storage account in the current subscription.</span></span>
<span data-ttu-id="61568-109">설정할 수 있는 속성은 **레이블** , **설명** , **형식** 및 **GeoReplicationEnabled** 입니다.</span><span class="sxs-lookup"><span data-stu-id="61568-109">Properties that can be set are: **Label** , **Description** , **Type** and **GeoReplicationEnabled**.</span></span>

## <span data-ttu-id="61568-110">예제의</span><span class="sxs-lookup"><span data-stu-id="61568-110">EXAMPLES</span></span>

### <span data-ttu-id="61568-111">예제 1: 저장소 계정의 레이블 업데이트</span><span class="sxs-lookup"><span data-stu-id="61568-111">Example 1: Update the label for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -Label "ContosoAccnt" -Description "Contoso storage account"
```

<span data-ttu-id="61568-112">이 명령은 ContosoStorage01 이라는 저장소 계정에 대 한 **레이블** 및 **설명** 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="61568-112">This command updates the **Label** and **Description** properties for the storage account named ContosoStorage01.</span></span>

### <span data-ttu-id="61568-113">예제 2: 저장소 계정에 대 한 지리적 복제 사용</span><span class="sxs-lookup"><span data-stu-id="61568-113">Example 2: Enable geo-replication for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $False
```

<span data-ttu-id="61568-114">이 명령은 **GeoReplicationEnabled** 속성을 ContosoStorage01 이라는 저장소 계정에 대 한 $False로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61568-114">This command sets the **GeoReplicationEnabled** property to $False for the storage account named ContosoStorage01.</span></span>

### <span data-ttu-id="61568-115">예제 3: 저장소 계정에 대 한 지리적 복제 비활성화</span><span class="sxs-lookup"><span data-stu-id="61568-115">Example 3: Disable geo-replication for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $True
```

<span data-ttu-id="61568-116">이 명령은 **GeoReplicationEnabled** 속성을 ContosoStorage01 이라는 저장소 계정에 대 한 $True로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61568-116">This command sets the **GeoReplicationEnabled** property to $True for the storage account named ContosoStorage01.</span></span>

## <span data-ttu-id="61568-117">변수</span><span class="sxs-lookup"><span data-stu-id="61568-117">PARAMETERS</span></span>

### <span data-ttu-id="61568-118">-설명</span><span class="sxs-lookup"><span data-stu-id="61568-118">-Description</span></span>
<span data-ttu-id="61568-119">저장소 계정에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61568-119">Specifies a description for the storage account.</span></span>
<span data-ttu-id="61568-120">설명은 최대 1024 자를 초과할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61568-120">The description may be up to 1024 characters long.</span></span>

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

### <span data-ttu-id="61568-121">-GeoReplicationEnabled</span><span class="sxs-lookup"><span data-stu-id="61568-121">-GeoReplicationEnabled</span></span>
<span data-ttu-id="61568-122">지리적 복제를 사용 하도록 설정 하 여 저장소 계정을 만들지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61568-122">Specifies whether the storage account is created with the geo-replication enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: GeoReplicationEnabled
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61568-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="61568-123">-InformationAction</span></span>
<span data-ttu-id="61568-124">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61568-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="61568-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="61568-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="61568-126">하기로</span><span class="sxs-lookup"><span data-stu-id="61568-126">Continue</span></span>
- <span data-ttu-id="61568-127">숨기기</span><span class="sxs-lookup"><span data-stu-id="61568-127">Ignore</span></span>
- <span data-ttu-id="61568-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="61568-128">Inquire</span></span>
- <span data-ttu-id="61568-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="61568-129">SilentlyContinue</span></span>
- <span data-ttu-id="61568-130">중지가</span><span class="sxs-lookup"><span data-stu-id="61568-130">Stop</span></span>
- <span data-ttu-id="61568-131">대기</span><span class="sxs-lookup"><span data-stu-id="61568-131">Suspend</span></span>

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

### <span data-ttu-id="61568-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="61568-132">-InformationVariable</span></span>
<span data-ttu-id="61568-133">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61568-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="61568-134">-레이블</span><span class="sxs-lookup"><span data-stu-id="61568-134">-Label</span></span>
<span data-ttu-id="61568-135">저장소 계정에 대 한 레이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61568-135">Specifies a label for the storage account.</span></span>
<span data-ttu-id="61568-136">레이블은 최대 100 자를 초과할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61568-136">The label may be up to 100 characters long.</span></span>

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

### <span data-ttu-id="61568-137">-프로필</span><span class="sxs-lookup"><span data-stu-id="61568-137">-Profile</span></span>
<span data-ttu-id="61568-138">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61568-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="61568-139">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="61568-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="61568-140">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="61568-140">-StorageAccountName</span></span>
<span data-ttu-id="61568-141">이 cmdlet이 수정 하는 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61568-141">Specifies the name of the storage account that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61568-142">-Type</span><span class="sxs-lookup"><span data-stu-id="61568-142">-Type</span></span>
<span data-ttu-id="61568-143">저장소 계정의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61568-143">Specifies the type of the storage account.</span></span>
<span data-ttu-id="61568-144">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="61568-144">Valid values are:</span></span> 

- <span data-ttu-id="61568-145">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="61568-145">Standard_LRS</span></span>
- <span data-ttu-id="61568-146">Standard_ZRS</span><span class="sxs-lookup"><span data-stu-id="61568-146">Standard_ZRS</span></span>
- <span data-ttu-id="61568-147">Standard_GRS</span><span class="sxs-lookup"><span data-stu-id="61568-147">Standard_GRS</span></span>
- <span data-ttu-id="61568-148">Standard_RAGRS</span><span class="sxs-lookup"><span data-stu-id="61568-148">Standard_RAGRS</span></span>
- <span data-ttu-id="61568-149">Premium_LRS</span><span class="sxs-lookup"><span data-stu-id="61568-149">Premium_LRS</span></span>

<span data-ttu-id="61568-150">이 매개 변수를 지정 하지 않을 경우 기본값은 Standard_GRS입니다.</span><span class="sxs-lookup"><span data-stu-id="61568-150">If this parameter is not specified, the default value is Standard_GRS.</span></span>

<span data-ttu-id="61568-151">*GeoReplicationEnabled* 매개 변수를 지정 하는 효과는 *형식* 매개 변수에 Standard_GRS를 지정 하는 것과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="61568-151">The effect of specifying the *GeoReplicationEnabled* parameter is the same as specifying Standard_GRS in the *Type* parameter.</span></span>

<span data-ttu-id="61568-152">Standard_ZRS 또는 Premium_LRS 계정은 다른 계정 유형으로 변경 하거나 그 반대의 경우도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="61568-152">Standard_ZRS or Premium_LRS accounts cannot be changed to other account types, and vice versa.</span></span>

```yaml
Type: String
Parameter Sets: AccountType
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61568-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61568-153">CommonParameters</span></span>
<span data-ttu-id="61568-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="61568-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61568-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61568-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61568-156">입력</span><span class="sxs-lookup"><span data-stu-id="61568-156">INPUTS</span></span>

## <span data-ttu-id="61568-157">출력</span><span class="sxs-lookup"><span data-stu-id="61568-157">OUTPUTS</span></span>

## <span data-ttu-id="61568-158">상속자</span><span class="sxs-lookup"><span data-stu-id="61568-158">NOTES</span></span>

## <span data-ttu-id="61568-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="61568-159">RELATED LINKS</span></span>

[<span data-ttu-id="61568-160">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="61568-160">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="61568-161">새-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="61568-161">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="61568-162">-AzureStorageAccount 제거</span><span class="sxs-lookup"><span data-stu-id="61568-162">Remove-AzureStorageAccount</span></span>](./Remove-AzureStorageAccount.md)


