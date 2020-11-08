---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 71302FB6-7E2B-4972-A743-AB537AC7CD79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79e194e0f8dda4392dec191881702c680bf172ac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046552"
---
# <span data-ttu-id="f1603-101">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="f1603-101">Get-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="f1603-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1603-102">SYNOPSIS</span></span>
<span data-ttu-id="f1603-103">서비스 구성의 액세스 제어 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f1603-103">Gets access control records in a service configuration.</span></span>

## <span data-ttu-id="f1603-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f1603-104">SYNTAX</span></span>

```
Get-AzureStorSimpleAccessControlRecord [-ACRName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f1603-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f1603-105">DESCRIPTION</span></span>
<span data-ttu-id="f1603-106">**AzureStorSimpleAccessControlRecord** Cmdlet은 StorSimple Manager 서비스 구성에서 액세스 제어 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f1603-106">The **Get-AzureStorSimpleAccessControlRecord** cmdlet gets access control records in the StorSimple Manager service configuration.</span></span>
<span data-ttu-id="f1603-107">이 cmdlet은 모든 레코드 또는 명명 된 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f1603-107">This cmdlet gets all records or a named record.</span></span>

<span data-ttu-id="f1603-108">액세스 제어 레코드는 iSCSI 초기자 매개 변수의 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="f1603-108">Access control records are containers of iSCSI initiator parameters.</span></span>
<span data-ttu-id="f1603-109">이러한 매개 변수는 볼륨에 액세스할 수 있는 초기자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1603-109">These parameters specify which initiators can access a volume.</span></span>
<span data-ttu-id="f1603-110">ISCSI 초기자가 볼륨에 대 한 연결을 시도 하면 기기는 해당 볼륨에 할당 된 액세스 제어 레코드를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1603-110">When an iSCSI initiator attempts to connect to a volume, your appliance checks the access control records assigned to that volume.</span></span>
<span data-ttu-id="f1603-111">ISCSI 초기자 매개 변수가 해당 볼륨에 매핑된 액세스 제어 레코드의 항목 중 하 나와 일치 하는 경우 iSCSI 초기자가 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f1603-111">If the iSCSI initiator parameters match one of the entries in an access control record mapped to that volume, the iSCSI initiator can connect.</span></span>

## <span data-ttu-id="f1603-112">예제의</span><span class="sxs-lookup"><span data-stu-id="f1603-112">EXAMPLES</span></span>

### <span data-ttu-id="f1603-113">예제 1: 모든 액세스 제어 레코드 가져오기</span><span class="sxs-lookup"><span data-stu-id="f1603-113">Example 1: Get all access control records</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord
InstanceId                           Name                        InitiatorName               VolumeCount
----------                           ----                        -------------               -----------
01a31aa5-14de-4b77-b926-2842577f540e Windows_XYUSFL718-RV_ACR    iqn.1991-05.com.microsof... 3
071c282d-0cd2-4c5f-b687-48966037ba48 Linux_XYUSFL719_ACR         iqn.1994-05.com.redhat:a... 3
4600eade-71f8-4d04-baec-0e7cf1d1e8fb Windows_XYUSFL720_ACR       iqn.1991-05.com.microsof... 9
d508d6f0-fcda-4624-b223-c0b307d6113e Linux_XYUSFL350_ACR         iqn.1991-05.com.microsof... 9
```

<span data-ttu-id="f1603-114">이 명령은 모든 액세스 제어 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f1603-114">This command gets all access control records.</span></span>

### <span data-ttu-id="f1603-115">예제 2: 특정 액세스 제어 레코드 가져오기</span><span class="sxs-lookup"><span data-stu-id="f1603-115">Example 2: Get a specific access control record</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr11"
VERBOSE: ClientRequestId: 61f261c7-acd3-4bcc-922a-ddfd85eb767b_PS
VERBOSE: ClientRequestId: 49c6a4c7-d299-46fd-a553-034c52b47487_PS

GlobalId            : 
InitiatorName       : iqn-contoso63
InstanceId          : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
Name                : Acr11
OperationInProgress : None
VolumeCount         : 6

VERBOSE: Access Control Record with given name Acr11 is found!
```

<span data-ttu-id="f1603-116">이 명령은 Acr11 이라는 액세스 제어 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f1603-116">This command gets the access control record named Acr11.</span></span>

## <span data-ttu-id="f1603-117">변수</span><span class="sxs-lookup"><span data-stu-id="f1603-117">PARAMETERS</span></span>

### <span data-ttu-id="f1603-118">-ACRName</span><span class="sxs-lookup"><span data-stu-id="f1603-118">-ACRName</span></span>
<span data-ttu-id="f1603-119">가져올 액세스 제어 레코드의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1603-119">Specifies the name of an access control record to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1603-120">-프로필</span><span class="sxs-lookup"><span data-stu-id="f1603-120">-Profile</span></span>
<span data-ttu-id="f1603-121">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1603-121">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="f1603-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1603-122">CommonParameters</span></span>
<span data-ttu-id="f1603-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1603-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1603-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1603-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1603-125">입력</span><span class="sxs-lookup"><span data-stu-id="f1603-125">INPUTS</span></span>

### <span data-ttu-id="f1603-126">않아야</span><span class="sxs-lookup"><span data-stu-id="f1603-126">None</span></span>

## <span data-ttu-id="f1603-127">출력</span><span class="sxs-lookup"><span data-stu-id="f1603-127">OUTPUTS</span></span>

### <span data-ttu-id="f1603-128">AccessControlRecord, IList\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="f1603-128">AccessControlRecord, IList\<AccessControlRecord\></span></span>
<span data-ttu-id="f1603-129">이 cmdlet은 **Accesscontrolrecord** 개체 또는 **\<AccessControlRecord\> IList** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1603-129">This cmdlet returns an **AccessControlRecord** object or an **IList\<AccessControlRecord\>** object.</span></span>
<span data-ttu-id="f1603-130">**Accesscontrolrecord** 개체에는 다음 필드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f1603-130">An **AccessControlRecord** object contains the following fields:</span></span> 

- <span data-ttu-id="f1603-131">**Globalid** ( **String** )</span><span class="sxs-lookup"><span data-stu-id="f1603-131">**GlobalId** ( **String** )</span></span> 
- <span data-ttu-id="f1603-132">**InitiatorName** ( **String** )</span><span class="sxs-lookup"><span data-stu-id="f1603-132">**InitiatorName** ( **String** )</span></span> 
- <span data-ttu-id="f1603-133">**InstanceId** ( **String** )</span><span class="sxs-lookup"><span data-stu-id="f1603-133">**InstanceId** ( **String** )</span></span> 
- <span data-ttu-id="f1603-134">**Name** ( **String** )</span><span class="sxs-lookup"><span data-stu-id="f1603-134">**Name** ( **String** )</span></span> 
- <span data-ttu-id="f1603-135">**Operationinprogress** ( **operationinprogress** )</span><span class="sxs-lookup"><span data-stu-id="f1603-135">**OperationInProgress** ( **OperationInProgress** )</span></span> 
- <span data-ttu-id="f1603-136">**(** **Int** ).</span><span class="sxs-lookup"><span data-stu-id="f1603-136">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="f1603-137">상속자</span><span class="sxs-lookup"><span data-stu-id="f1603-137">NOTES</span></span>

## <span data-ttu-id="f1603-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1603-138">RELATED LINKS</span></span>

[<span data-ttu-id="f1603-139">새로운 AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="f1603-139">New-AzureStorSimpleAccessControlRecord</span></span>](./New-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="f1603-140">제거-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="f1603-140">Remove-AzureStorSimpleAccessControlRecord</span></span>](./Remove-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="f1603-141">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="f1603-141">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)


