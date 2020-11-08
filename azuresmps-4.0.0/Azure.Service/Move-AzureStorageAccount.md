---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6AFD3971-460D-4F6A-B266-6ED98DC81CD4
online version: ''
schema: 2.0.0
ms.openlocfilehash: c007e3a318067f29da6ea710c25cf2c52d5df2b4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046239"
---
# <span data-ttu-id="21060-101">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="21060-101">Move-AzureStorageAccount</span></span>

## <span data-ttu-id="21060-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21060-102">SYNOPSIS</span></span>
<span data-ttu-id="21060-103">Azure 리소스 관리자 스택으로 저장소 계정을 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="21060-103">Migrates a storage account to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="21060-104">구문과</span><span class="sxs-lookup"><span data-stu-id="21060-104">SYNTAX</span></span>

### <span data-ttu-id="21060-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="21060-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Validate] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="21060-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="21060-106">AbortMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Abort] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="21060-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="21060-107">CommitMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Commit] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="21060-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="21060-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Prepare] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="21060-109">설명은</span><span class="sxs-lookup"><span data-stu-id="21060-109">DESCRIPTION</span></span>
<span data-ttu-id="21060-110">**이동-AzureStorageAccount** cmdlet은 저장소 계정을 Azure 리소스 관리자 스택의 리소스 그룹으로 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="21060-110">The **Move-AzureStorageAccount** cmdlet migrates a storage account to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="21060-111">예제의</span><span class="sxs-lookup"><span data-stu-id="21060-111">EXAMPLES</span></span>

### <span data-ttu-id="21060-112">예제 1: 저장소 계정 마이그레이션 준비</span><span class="sxs-lookup"><span data-stu-id="21060-112">Example 1: Prepare storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Prepare -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="21060-113">이 명령은 ContosoStorageName 이라는 저장소 계정을 Azure 리소스 관리자 스택으로 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="21060-113">This command prepares the storage account named ContosoStorageName for migration to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="21060-114">예제 2: 저장소 계정 마이그레이션 시작</span><span class="sxs-lookup"><span data-stu-id="21060-114">Example 2: Start storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Commit -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="21060-115">이 명령은 ContosoStorageName 이라는 저장소 계정에 대 한 마이그레이션을 시작 하 여 Azure Resource Manager 스택에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="21060-115">This command starts migration of the storage account named ContosoStorageName to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="21060-116">예제 3: 저장소 계정 마이그레이션 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="21060-116">Example 3: Validate storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Validate -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="21060-117">이 명령은 ContosoStorageName 이라는 저장소 계정에 대 한 마이그레이션을 유효성 검사 하 여 Azure Resource Manager 스택에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21060-117">This command validates migration for the storage account named ContosoStorageName to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="21060-118">변수</span><span class="sxs-lookup"><span data-stu-id="21060-118">PARAMETERS</span></span>

### <span data-ttu-id="21060-119">-Abort</span><span class="sxs-lookup"><span data-stu-id="21060-119">-Abort</span></span>
<span data-ttu-id="21060-120">이 cmdlet이 저장소 계정 마이그레이션을 취소 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="21060-120">Indicates that this cmdlet cancels the storage account migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AbortMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21060-121">-커밋</span><span class="sxs-lookup"><span data-stu-id="21060-121">-Commit</span></span>
<span data-ttu-id="21060-122">이 cmdlet이 저장소 계정 마이그레이션을 시작 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="21060-122">Indicates that this cmdlet starts the storage account migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CommitMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21060-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="21060-123">-InformationAction</span></span>
<span data-ttu-id="21060-124">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21060-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="21060-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="21060-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="21060-126">하기로</span><span class="sxs-lookup"><span data-stu-id="21060-126">Continue</span></span>
- <span data-ttu-id="21060-127">숨기기</span><span class="sxs-lookup"><span data-stu-id="21060-127">Ignore</span></span>
- <span data-ttu-id="21060-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="21060-128">Inquire</span></span>
- <span data-ttu-id="21060-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="21060-129">SilentlyContinue</span></span>
- <span data-ttu-id="21060-130">중지가</span><span class="sxs-lookup"><span data-stu-id="21060-130">Stop</span></span>
- <span data-ttu-id="21060-131">대기</span><span class="sxs-lookup"><span data-stu-id="21060-131">Suspend</span></span>

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

### <span data-ttu-id="21060-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="21060-132">-InformationVariable</span></span>
<span data-ttu-id="21060-133">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21060-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="21060-134">-준비</span><span class="sxs-lookup"><span data-stu-id="21060-134">-Prepare</span></span>
<span data-ttu-id="21060-135">이 cmdlet이 마이그레이션을 위해 저장소 계정을 준비 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="21060-135">Indicates that this cmdlet prepares the storage account for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21060-136">-프로필</span><span class="sxs-lookup"><span data-stu-id="21060-136">-Profile</span></span>
<span data-ttu-id="21060-137">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21060-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="21060-138">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="21060-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="21060-139">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="21060-139">-StorageAccountName</span></span>
<span data-ttu-id="21060-140">이 cmdlet이 마이그레이션하는 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21060-140">Specifies the name of the storage account that this cmdlet migrates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21060-141">-유효성 검사</span><span class="sxs-lookup"><span data-stu-id="21060-141">-Validate</span></span>
<span data-ttu-id="21060-142">이 cmdlet이 마이그레이션을 위해 저장소 계정의 유효성을 검사 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21060-142">Specifies that this cmdlet validates the storage account for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21060-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21060-143">CommonParameters</span></span>
<span data-ttu-id="21060-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="21060-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21060-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21060-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21060-146">입력</span><span class="sxs-lookup"><span data-stu-id="21060-146">INPUTS</span></span>

## <span data-ttu-id="21060-147">출력</span><span class="sxs-lookup"><span data-stu-id="21060-147">OUTPUTS</span></span>

## <span data-ttu-id="21060-148">상속자</span><span class="sxs-lookup"><span data-stu-id="21060-148">NOTES</span></span>

## <span data-ttu-id="21060-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="21060-149">RELATED LINKS</span></span>

[<span data-ttu-id="21060-150">이동-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="21060-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="21060-151">이동-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="21060-151">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="21060-152">이동-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="21060-152">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="21060-153">이동-AzureService</span><span class="sxs-lookup"><span data-stu-id="21060-153">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="21060-154">이동-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="21060-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


