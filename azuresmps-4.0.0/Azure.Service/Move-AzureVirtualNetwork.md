---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2B0CC65A-0A73-4FFE-BF7C-B148871909D9
online version: ''
schema: 2.0.0
ms.openlocfilehash: df768878bf26c186751171edf7ed41acb3f7d15a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046238"
---
# <span data-ttu-id="b2f5f-101">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b2f5f-101">Move-AzureVirtualNetwork</span></span>

## <span data-ttu-id="b2f5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2f5f-102">SYNOPSIS</span></span>
<span data-ttu-id="b2f5f-103">가상 네트워크를 Azure Resource Manager 스택으로 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f5f-103">Migrates a virtual network to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="b2f5f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b2f5f-104">SYNTAX</span></span>

### <span data-ttu-id="b2f5f-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2f5f-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2f5f-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2f5f-106">AbortMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2f5f-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2f5f-107">CommitMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2f5f-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2f5f-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b2f5f-109">설명은</span><span class="sxs-lookup"><span data-stu-id="b2f5f-109">DESCRIPTION</span></span>
<span data-ttu-id="b2f5f-110">**AzureVirtualNetwork** cmdlet은 가상 네트워크를 Azure resource Manager 스택의 리소스 그룹으로 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f5f-110">The **Move-AzureVirtualNetwork** cmdlet migrates a virtual network to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="b2f5f-111">예제의</span><span class="sxs-lookup"><span data-stu-id="b2f5f-111">EXAMPLES</span></span>

### <span data-ttu-id="b2f5f-112">예제 1: 가상 네트워크 마이그레이션 준비</span><span class="sxs-lookup"><span data-stu-id="b2f5f-112">Example 1: Prepare virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Prepare -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="b2f5f-113">이 명령은 ContosoVNET 이라는 가상 네트워크를 Azure 리소스 관리자 스택으로 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f5f-113">This command prepares the virtual network named ContosoVNET for migration to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="b2f5f-114">예제 2: 가상 네트워크 마이그레이션 시작</span><span class="sxs-lookup"><span data-stu-id="b2f5f-114">Example 2: Start virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Commit -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="b2f5f-115">이 명령은 ContosoVNET 이라는 가상 네트워크의 마이그레이션을 Azure Resource Manager 스택으로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f5f-115">This command starts migration of the virtual network named ContosoVNET to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="b2f5f-116">예제 3: 가상 네트워크 마이그레이션 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="b2f5f-116">Example 3: Validate virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Validate -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="b2f5f-117">이 명령은 ContosoVNET 이라는 가상 네트워크의 마이그레이션을 Azure Resource Manager 스택에 대해 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f5f-117">This command validates migration for the virtual network named ContosoVNET to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="b2f5f-118">변수</span><span class="sxs-lookup"><span data-stu-id="b2f5f-118">PARAMETERS</span></span>

### <span data-ttu-id="b2f5f-119">-Abort</span><span class="sxs-lookup"><span data-stu-id="b2f5f-119">-Abort</span></span>
<span data-ttu-id="b2f5f-120">이 cmdlet이 가상 네트워크 마이그레이션을 취소 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b2f5f-120">Indicates that this cmdlet cancels the virtual network migration.</span></span>

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

### <span data-ttu-id="b2f5f-121">-커밋</span><span class="sxs-lookup"><span data-stu-id="b2f5f-121">-Commit</span></span>
<span data-ttu-id="b2f5f-122">이 cmdlet이 가상 네트워크 마이그레이션을 시작 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b2f5f-122">Indicates that this cmdlet starts the virtual network migration.</span></span>

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

### <span data-ttu-id="b2f5f-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b2f5f-123">-InformationAction</span></span>
<span data-ttu-id="b2f5f-124">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f5f-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b2f5f-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b2f5f-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b2f5f-126">하기로</span><span class="sxs-lookup"><span data-stu-id="b2f5f-126">Continue</span></span>
- <span data-ttu-id="b2f5f-127">숨기기</span><span class="sxs-lookup"><span data-stu-id="b2f5f-127">Ignore</span></span>
- <span data-ttu-id="b2f5f-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="b2f5f-128">Inquire</span></span>
- <span data-ttu-id="b2f5f-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b2f5f-129">SilentlyContinue</span></span>
- <span data-ttu-id="b2f5f-130">중지가</span><span class="sxs-lookup"><span data-stu-id="b2f5f-130">Stop</span></span>
- <span data-ttu-id="b2f5f-131">대기</span><span class="sxs-lookup"><span data-stu-id="b2f5f-131">Suspend</span></span>

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

### <span data-ttu-id="b2f5f-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b2f5f-132">-InformationVariable</span></span>
<span data-ttu-id="b2f5f-133">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f5f-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b2f5f-134">-준비</span><span class="sxs-lookup"><span data-stu-id="b2f5f-134">-Prepare</span></span>
<span data-ttu-id="b2f5f-135">이 cmdlet이 마이그레이션을 위해 가상 네트워크를 준비 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b2f5f-135">Indicates that this cmdlet prepares the virtual network for migration.</span></span>

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

### <span data-ttu-id="b2f5f-136">-프로필</span><span class="sxs-lookup"><span data-stu-id="b2f5f-136">-Profile</span></span>
<span data-ttu-id="b2f5f-137">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f5f-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b2f5f-138">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b2f5f-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b2f5f-139">-유효성 검사</span><span class="sxs-lookup"><span data-stu-id="b2f5f-139">-Validate</span></span>
<span data-ttu-id="b2f5f-140">이 cmdlet이 마이그레이션을 위해 가상 네트워크의 유효성을 검사 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f5f-140">Specifies that this cmdlet validates the virtual network for migration.</span></span>

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

### <span data-ttu-id="b2f5f-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="b2f5f-141">-VirtualNetworkName</span></span>
<span data-ttu-id="b2f5f-142">마이그레이션할 가상 네트워크의 이름</span><span class="sxs-lookup"><span data-stu-id="b2f5f-142">Name of the Virtual Network to migrate</span></span>

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

### <span data-ttu-id="b2f5f-143">-확인</span><span class="sxs-lookup"><span data-stu-id="b2f5f-143">-Confirm</span></span>
<span data-ttu-id="b2f5f-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f5f-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2f5f-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2f5f-145">-WhatIf</span></span>
<span data-ttu-id="b2f5f-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b2f5f-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2f5f-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b2f5f-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2f5f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2f5f-148">CommonParameters</span></span>
<span data-ttu-id="b2f5f-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f5f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2f5f-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2f5f-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2f5f-151">입력</span><span class="sxs-lookup"><span data-stu-id="b2f5f-151">INPUTS</span></span>

## <span data-ttu-id="b2f5f-152">출력</span><span class="sxs-lookup"><span data-stu-id="b2f5f-152">OUTPUTS</span></span>

## <span data-ttu-id="b2f5f-153">상속자</span><span class="sxs-lookup"><span data-stu-id="b2f5f-153">NOTES</span></span>

## <span data-ttu-id="b2f5f-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2f5f-154">RELATED LINKS</span></span>

[<span data-ttu-id="b2f5f-155">이동-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b2f5f-155">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="b2f5f-156">이동-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="b2f5f-156">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="b2f5f-157">이동-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="b2f5f-157">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="b2f5f-158">이동-AzureService</span><span class="sxs-lookup"><span data-stu-id="b2f5f-158">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="b2f5f-159">이동-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b2f5f-159">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)


