---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D1A4FA07-C25E-472B-9C64-695AD41274FA
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb8b6a502d6abe5520cadcf776ece1f077c7d91f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046242"
---
# <span data-ttu-id="90fd6-101">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="90fd6-101">Move-AzureReservedIP</span></span>

## <span data-ttu-id="90fd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90fd6-102">SYNOPSIS</span></span>
<span data-ttu-id="90fd6-103">예약 된 IP 주소를 Azure 리소스 관리자 스택으로 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="90fd6-103">Migrates a reserved IP address to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="90fd6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="90fd6-104">SYNTAX</span></span>

### <span data-ttu-id="90fd6-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="90fd6-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90fd6-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="90fd6-106">AbortMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90fd6-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="90fd6-107">CommitMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90fd6-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="90fd6-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="90fd6-109">설명은</span><span class="sxs-lookup"><span data-stu-id="90fd6-109">DESCRIPTION</span></span>
<span data-ttu-id="90fd6-110">**AzureReservedIP** cmdlet은 예약 된 IP 주소를 Azure resource Manager 스택의 리소스 그룹으로 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="90fd6-110">The **Move-AzureReservedIP** cmdlet migrates a reserved IP address to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="90fd6-111">예제의</span><span class="sxs-lookup"><span data-stu-id="90fd6-111">EXAMPLES</span></span>

### <span data-ttu-id="90fd6-112">raid-1</span><span class="sxs-lookup"><span data-stu-id="90fd6-112">1:</span></span>
```

```

## <span data-ttu-id="90fd6-113">변수</span><span class="sxs-lookup"><span data-stu-id="90fd6-113">PARAMETERS</span></span>

### <span data-ttu-id="90fd6-114">-Abort</span><span class="sxs-lookup"><span data-stu-id="90fd6-114">-Abort</span></span>
<span data-ttu-id="90fd6-115">이 cmdlet이 예약 된 IP 주소 마이그레이션을 취소 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="90fd6-115">Indicates that this cmdlet cancels the reserved IP address migration.</span></span>

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

### <span data-ttu-id="90fd6-116">-커밋</span><span class="sxs-lookup"><span data-stu-id="90fd6-116">-Commit</span></span>
<span data-ttu-id="90fd6-117">이 cmdlet이 예약 된 IP 주소 마이그레이션을 시작 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="90fd6-117">Indicates that this cmdlet starts the reserved IP address migration.</span></span>

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

### <span data-ttu-id="90fd6-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="90fd6-118">-InformationAction</span></span>
<span data-ttu-id="90fd6-119">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90fd6-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="90fd6-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="90fd6-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="90fd6-121">하기로</span><span class="sxs-lookup"><span data-stu-id="90fd6-121">Continue</span></span>
- <span data-ttu-id="90fd6-122">숨기기</span><span class="sxs-lookup"><span data-stu-id="90fd6-122">Ignore</span></span>
- <span data-ttu-id="90fd6-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="90fd6-123">Inquire</span></span>
- <span data-ttu-id="90fd6-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="90fd6-124">SilentlyContinue</span></span>
- <span data-ttu-id="90fd6-125">중지가</span><span class="sxs-lookup"><span data-stu-id="90fd6-125">Stop</span></span>
- <span data-ttu-id="90fd6-126">대기</span><span class="sxs-lookup"><span data-stu-id="90fd6-126">Suspend</span></span>

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

### <span data-ttu-id="90fd6-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="90fd6-127">-InformationVariable</span></span>
<span data-ttu-id="90fd6-128">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90fd6-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="90fd6-129">-준비</span><span class="sxs-lookup"><span data-stu-id="90fd6-129">-Prepare</span></span>
<span data-ttu-id="90fd6-130">이 cmdlet이 마이그레이션에 예약 된 IP 주소를 준비 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="90fd6-130">Indicates that this cmdlet prepares the reserved IP address for migration.</span></span>

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

### <span data-ttu-id="90fd6-131">-프로필</span><span class="sxs-lookup"><span data-stu-id="90fd6-131">-Profile</span></span>
<span data-ttu-id="90fd6-132">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90fd6-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="90fd6-133">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="90fd6-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="90fd6-134">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="90fd6-134">-ReservedIPName</span></span>
<span data-ttu-id="90fd6-135">이 cmdlet이 마이그레이션하는 예약 된 IP 주소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90fd6-135">Specifies the name of the reserved IP address that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="90fd6-136">-유효성 검사</span><span class="sxs-lookup"><span data-stu-id="90fd6-136">-Validate</span></span>
<span data-ttu-id="90fd6-137">이 cmdlet이 마이그레이션에 예약 된 IP 주소의 유효성을 검사 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90fd6-137">Specifies that this cmdlet validates the reserved IP address for migration.</span></span>

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

### <span data-ttu-id="90fd6-138">-확인</span><span class="sxs-lookup"><span data-stu-id="90fd6-138">-Confirm</span></span>
<span data-ttu-id="90fd6-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="90fd6-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90fd6-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90fd6-140">-WhatIf</span></span>
<span data-ttu-id="90fd6-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="90fd6-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90fd6-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90fd6-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90fd6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90fd6-143">CommonParameters</span></span>
<span data-ttu-id="90fd6-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="90fd6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90fd6-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90fd6-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90fd6-146">입력</span><span class="sxs-lookup"><span data-stu-id="90fd6-146">INPUTS</span></span>

## <span data-ttu-id="90fd6-147">출력</span><span class="sxs-lookup"><span data-stu-id="90fd6-147">OUTPUTS</span></span>

## <span data-ttu-id="90fd6-148">상속자</span><span class="sxs-lookup"><span data-stu-id="90fd6-148">NOTES</span></span>

## <span data-ttu-id="90fd6-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90fd6-149">RELATED LINKS</span></span>

[<span data-ttu-id="90fd6-150">이동-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="90fd6-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="90fd6-151">이동-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="90fd6-151">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="90fd6-152">이동-AzureService</span><span class="sxs-lookup"><span data-stu-id="90fd6-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="90fd6-153">이동-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="90fd6-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="90fd6-154">이동-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="90fd6-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


