---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 01213154-DD8A-412F-A23D-5D9D09BEFA3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: f0602015a63d28aecb498b0830619ea1560d6066
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046241"
---
# <span data-ttu-id="2b8c5-101">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="2b8c5-101">Move-AzureRouteTable</span></span>

## <span data-ttu-id="2b8c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b8c5-102">SYNOPSIS</span></span>
<span data-ttu-id="2b8c5-103">Azure Resource Manager 스택으로 경로 테이블을 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="2b8c5-103">Migrates a route table to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="2b8c5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2b8c5-104">SYNTAX</span></span>

### <span data-ttu-id="2b8c5-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b8c5-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b8c5-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b8c5-106">AbortMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b8c5-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b8c5-107">CommitMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b8c5-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b8c5-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b8c5-109">설명은</span><span class="sxs-lookup"><span data-stu-id="2b8c5-109">DESCRIPTION</span></span>
<span data-ttu-id="2b8c5-110">**AzureRouteTable** cmdlet은 경로 테이블을 Azure resource Manager 스택의 리소스 그룹으로 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="2b8c5-110">The **Move-AzureRouteTable** cmdlet migrates a route table to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="2b8c5-111">예제의</span><span class="sxs-lookup"><span data-stu-id="2b8c5-111">EXAMPLES</span></span>

### <span data-ttu-id="2b8c5-112">raid-1</span><span class="sxs-lookup"><span data-stu-id="2b8c5-112">1:</span></span>
```

```

## <span data-ttu-id="2b8c5-113">변수</span><span class="sxs-lookup"><span data-stu-id="2b8c5-113">PARAMETERS</span></span>

### <span data-ttu-id="2b8c5-114">-Abort</span><span class="sxs-lookup"><span data-stu-id="2b8c5-114">-Abort</span></span>
<span data-ttu-id="2b8c5-115">이 cmdlet이 경로 테이블 마이그레이션을 취소 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2b8c5-115">Indicates that this cmdlet cancels the route table migration.</span></span>

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

### <span data-ttu-id="2b8c5-116">-커밋</span><span class="sxs-lookup"><span data-stu-id="2b8c5-116">-Commit</span></span>
<span data-ttu-id="2b8c5-117">이 cmdlet이 경로 테이블 마이그레이션을 시작 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2b8c5-117">Indicates that this cmdlet starts the route table migration.</span></span>

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

### <span data-ttu-id="2b8c5-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2b8c5-118">-InformationAction</span></span>
<span data-ttu-id="2b8c5-119">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b8c5-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2b8c5-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2b8c5-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2b8c5-121">하기로</span><span class="sxs-lookup"><span data-stu-id="2b8c5-121">Continue</span></span>
- <span data-ttu-id="2b8c5-122">숨기기</span><span class="sxs-lookup"><span data-stu-id="2b8c5-122">Ignore</span></span>
- <span data-ttu-id="2b8c5-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="2b8c5-123">Inquire</span></span>
- <span data-ttu-id="2b8c5-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2b8c5-124">SilentlyContinue</span></span>
- <span data-ttu-id="2b8c5-125">중지가</span><span class="sxs-lookup"><span data-stu-id="2b8c5-125">Stop</span></span>
- <span data-ttu-id="2b8c5-126">대기</span><span class="sxs-lookup"><span data-stu-id="2b8c5-126">Suspend</span></span>

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

### <span data-ttu-id="2b8c5-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2b8c5-127">-InformationVariable</span></span>
<span data-ttu-id="2b8c5-128">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b8c5-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2b8c5-129">-준비</span><span class="sxs-lookup"><span data-stu-id="2b8c5-129">-Prepare</span></span>
<span data-ttu-id="2b8c5-130">이 cmdlet이 마이그레이션에 대 한 경로 테이블을 준비 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2b8c5-130">Indicates that this cmdlet prepares the route table for migration.</span></span>

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

### <span data-ttu-id="2b8c5-131">-프로필</span><span class="sxs-lookup"><span data-stu-id="2b8c5-131">-Profile</span></span>
<span data-ttu-id="2b8c5-132">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b8c5-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2b8c5-133">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="2b8c5-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2b8c5-134">-RouteTableName</span><span class="sxs-lookup"><span data-stu-id="2b8c5-134">-RouteTableName</span></span>
<span data-ttu-id="2b8c5-135">이 cmdlet이 마이그레이션하는 경로 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b8c5-135">Specifies the name of the route table that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="2b8c5-136">-유효성 검사</span><span class="sxs-lookup"><span data-stu-id="2b8c5-136">-Validate</span></span>
<span data-ttu-id="2b8c5-137">이 cmdlet이 마이그레이션에 대 한 경로 테이블의 유효성을 검사 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b8c5-137">Specifies that this cmdlet validates the route table for migration.</span></span>

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

### <span data-ttu-id="2b8c5-138">-확인</span><span class="sxs-lookup"><span data-stu-id="2b8c5-138">-Confirm</span></span>
<span data-ttu-id="2b8c5-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b8c5-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b8c5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b8c5-140">-WhatIf</span></span>
<span data-ttu-id="2b8c5-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2b8c5-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b8c5-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2b8c5-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b8c5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b8c5-143">CommonParameters</span></span>
<span data-ttu-id="2b8c5-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b8c5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b8c5-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b8c5-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b8c5-146">입력</span><span class="sxs-lookup"><span data-stu-id="2b8c5-146">INPUTS</span></span>

## <span data-ttu-id="2b8c5-147">출력</span><span class="sxs-lookup"><span data-stu-id="2b8c5-147">OUTPUTS</span></span>

## <span data-ttu-id="2b8c5-148">상속자</span><span class="sxs-lookup"><span data-stu-id="2b8c5-148">NOTES</span></span>

## <span data-ttu-id="2b8c5-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b8c5-149">RELATED LINKS</span></span>

[<span data-ttu-id="2b8c5-150">이동-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2b8c5-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="2b8c5-151">이동-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="2b8c5-151">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="2b8c5-152">이동-AzureService</span><span class="sxs-lookup"><span data-stu-id="2b8c5-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="2b8c5-153">이동-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2b8c5-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="2b8c5-154">이동-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2b8c5-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


