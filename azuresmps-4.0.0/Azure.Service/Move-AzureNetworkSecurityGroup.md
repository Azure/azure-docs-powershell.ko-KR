---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 27ECCBAD-0CFE-4309-B590-BB60E1872ED5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d96f02374eb266cb9eaa3c1cc7c200a4f154043
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046243"
---
# <span data-ttu-id="2fd77-101">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2fd77-101">Move-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="2fd77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fd77-102">SYNOPSIS</span></span>
<span data-ttu-id="2fd77-103">네트워크 보안 그룹을 Azure Resource Manager 스택으로 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="2fd77-103">Migrates a Network Security Group to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="2fd77-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2fd77-104">SYNTAX</span></span>

### <span data-ttu-id="2fd77-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fd77-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2fd77-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fd77-106">AbortMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2fd77-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fd77-107">CommitMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2fd77-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fd77-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2fd77-109">설명은</span><span class="sxs-lookup"><span data-stu-id="2fd77-109">DESCRIPTION</span></span>
<span data-ttu-id="2fd77-110">**AzureNetworkSecurityGroup** Cmdlet은 네트워크 보안 그룹을 Azure resource Manager 스택의 리소스 그룹으로 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="2fd77-110">The **Move-AzureNetworkSecurityGroup** cmdlet migrates a Network Security Group to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="2fd77-111">예제의</span><span class="sxs-lookup"><span data-stu-id="2fd77-111">EXAMPLES</span></span>

### <span data-ttu-id="2fd77-112">raid-1</span><span class="sxs-lookup"><span data-stu-id="2fd77-112">1:</span></span>
```

```

## <span data-ttu-id="2fd77-113">변수</span><span class="sxs-lookup"><span data-stu-id="2fd77-113">PARAMETERS</span></span>

### <span data-ttu-id="2fd77-114">-Abort</span><span class="sxs-lookup"><span data-stu-id="2fd77-114">-Abort</span></span>
<span data-ttu-id="2fd77-115">이 cmdlet이 네트워크 보안 그룹 마이그레이션을 취소 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2fd77-115">Indicates that this cmdlet cancels the Network Security Group migration.</span></span>

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

### <span data-ttu-id="2fd77-116">-커밋</span><span class="sxs-lookup"><span data-stu-id="2fd77-116">-Commit</span></span>
<span data-ttu-id="2fd77-117">이 cmdlet이 네트워크 보안 그룹 마이그레이션을 시작 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2fd77-117">Indicates that this cmdlet starts the Network Security Group migration.</span></span>

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

### <span data-ttu-id="2fd77-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2fd77-118">-InformationAction</span></span>
<span data-ttu-id="2fd77-119">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fd77-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2fd77-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2fd77-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2fd77-121">하기로</span><span class="sxs-lookup"><span data-stu-id="2fd77-121">Continue</span></span>
- <span data-ttu-id="2fd77-122">숨기기</span><span class="sxs-lookup"><span data-stu-id="2fd77-122">Ignore</span></span>
- <span data-ttu-id="2fd77-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="2fd77-123">Inquire</span></span>
- <span data-ttu-id="2fd77-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2fd77-124">SilentlyContinue</span></span>
- <span data-ttu-id="2fd77-125">중지가</span><span class="sxs-lookup"><span data-stu-id="2fd77-125">Stop</span></span>
- <span data-ttu-id="2fd77-126">대기</span><span class="sxs-lookup"><span data-stu-id="2fd77-126">Suspend</span></span>

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

### <span data-ttu-id="2fd77-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2fd77-127">-InformationVariable</span></span>
<span data-ttu-id="2fd77-128">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fd77-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2fd77-129">-NetworkSecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="2fd77-129">-NetworkSecurityGroupName</span></span>
<span data-ttu-id="2fd77-130">이 cmdlet이 마이그레이션하는 네트워크 보안 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fd77-130">Specifies the name of the Network Security Group that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="2fd77-131">-준비</span><span class="sxs-lookup"><span data-stu-id="2fd77-131">-Prepare</span></span>
<span data-ttu-id="2fd77-132">이 cmdlet이 마이그레이션을 위해 네트워크 보안 그룹을 준비 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2fd77-132">Indicates that this cmdlet prepares the Network Security Group for migration.</span></span>

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

### <span data-ttu-id="2fd77-133">-프로필</span><span class="sxs-lookup"><span data-stu-id="2fd77-133">-Profile</span></span>
<span data-ttu-id="2fd77-134">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fd77-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2fd77-135">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="2fd77-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2fd77-136">-유효성 검사</span><span class="sxs-lookup"><span data-stu-id="2fd77-136">-Validate</span></span>
<span data-ttu-id="2fd77-137">이 cmdlet이 마이그레이션을 위해 네트워크 보안 그룹의 유효성을 검사 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fd77-137">Specifies that this cmdlet validates the Network Security Group for migration.</span></span>

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

### <span data-ttu-id="2fd77-138">-확인</span><span class="sxs-lookup"><span data-stu-id="2fd77-138">-Confirm</span></span>
<span data-ttu-id="2fd77-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fd77-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fd77-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fd77-140">-WhatIf</span></span>
<span data-ttu-id="2fd77-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2fd77-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fd77-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2fd77-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fd77-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fd77-143">CommonParameters</span></span>
<span data-ttu-id="2fd77-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fd77-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fd77-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fd77-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fd77-146">입력</span><span class="sxs-lookup"><span data-stu-id="2fd77-146">INPUTS</span></span>

## <span data-ttu-id="2fd77-147">출력</span><span class="sxs-lookup"><span data-stu-id="2fd77-147">OUTPUTS</span></span>

## <span data-ttu-id="2fd77-148">상속자</span><span class="sxs-lookup"><span data-stu-id="2fd77-148">NOTES</span></span>

## <span data-ttu-id="2fd77-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2fd77-149">RELATED LINKS</span></span>

[<span data-ttu-id="2fd77-150">이동-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="2fd77-150">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="2fd77-151">이동-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="2fd77-151">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="2fd77-152">이동-AzureService</span><span class="sxs-lookup"><span data-stu-id="2fd77-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="2fd77-153">이동-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2fd77-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="2fd77-154">이동-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2fd77-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


